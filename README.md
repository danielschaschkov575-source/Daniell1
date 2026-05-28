# YouTube zu MP3 Converter 🎵

Ein einfaches CLI-Tool zur Konvertierung von YouTube Videos und Playlists zu MP3-Dateien mit verschiedenen Qualitätseinstellungen.

## Features ✨

- ✅ Download einzelner YouTube Videos
- ✅ Download kompletter Playlists
- ✅ Verschiedene Qualitätseinstellungen (128, 192, 320 kbps)
- ✅ Benutzerdefinierte Bitrate möglich
- ✅ Farbige Ausgabe im Terminal
- ✅ Fortschrittsanzeige
- ✅ Fehlerbehandlung

## Anforderungen 📋

- Python 3.8+
- ffmpeg (für Audio-Konvertierung)
- Internetverbindung

### ffmpeg installieren

**Auf Ubuntu/Debian:**
```bash
sudo apt-get install ffmpeg
```

**Auf macOS (mit Homebrew):**
```bash
brew install ffmpeg
```

**Auf Windows:**
Laden Sie ffmpeg von https://ffmpeg.org/download.html herunter oder nutzen Sie:
```bash
choco install ffmpeg
```

## Installation 🔧

1. **Repository klonen/öffnen:**
```bash
cd /workspaces/Daniell1
```

2. **Python-Abhängigkeiten installieren:**
```bash
pip install -r requirements.txt
```

## Verwendung 📖

### Einfaches Beispiel - Einzelnes Video

```bash
python youtube_to_mp3.py "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
```

### Mit Qualitätseinstellung

```bash
# Hohe Qualität (320 kbps)
python youtube_to_mp3.py "https://www.youtube.com/watch?v=..." -q high

# Mittlere Qualität (192 kbps) - Standard
python youtube_to_mp3.py "https://www.youtube.com/watch?v=..." -q medium

# Niedrige Qualität (128 kbps)
python youtube_to_mp3.py "https://www.youtube.com/watch?v=..." -q low
```

### Playlist herunterladen

```bash
python youtube_to_mp3.py "https://www.youtube.com/playlist?list=..." -q high
```

### Benutzerdefinierten Ordner angeben

```bash
python youtube_to_mp3.py "https://www.youtube.com/watch?v=..." -o ./meine_musik
```

### Alle Optionen anzeigen

```bash
python youtube_to_mp3.py --help
```

## Kommandozeilenoptionen 🎮

| Option | Kurz | Beschreibung |
|--------|------|-------------|
| `--output` | `-o` | Ausgabeverzeichnis (Standard: `./downloads`) |
| `--quality` | `-q` | Qualität: `low`, `medium`, `high` (Standard: `medium`) |
| `--bitrate` | `-b` | Benutzerdefinierte Bitrate in kbps |
| `--help` | `-h` | Hilfe anzeigen |

## Qualitätspresets 🎚️

| Preset | Bitrate | Speicher pro Minute |
|--------|---------|-------------------|
| low | 128 kbps | ~0.96 MB |
| medium | 192 kbps | ~1.44 MB |
| high | 320 kbps | ~2.4 MB |

## Beispiele 💡

```bash
# Musik von YouTube herunterladen und in hoher Qualität speichern
python youtube_to_mp3.py "https://www.youtube.com/watch?v=xyz123" -q high -o ./musik

# Komplette Playlist mit benutzerdefinierten Einstellungen
python youtube_to_mp3.py "https://www.youtube.com/playlist?list=PLxxx" -b 256 -o ./playlists

# Mit Fortschrittsanzeige
python youtube_to_mp3.py "https://www.youtube.com/watch?v=xyz123"
```

## Troubleshooting 🔍

### "ffmpeg nicht gefunden"
Stellen Sie sicher, dass ffmpeg installiert und in Ihrem PATH ist:
```bash
which ffmpeg  # Linux/Mac
where ffmpeg  # Windows
```

### "Video nicht herunterladbar"
- Überprüfen Sie, ob die URL korrekt ist
- Manche Videos könnten geografische Beschränkungen haben
- Versuchen Sie, yt-dlp zu aktualisieren: `pip install --upgrade yt-dlp`

### "ModuleNotFoundError"
Installieren Sie die Abhängigkeiten neu:
```bash
pip install -r requirements.txt
```

## Lizenz 📜

MIT License

## Hinweise ⚠️

- Beachten Sie die Urheberrechte beim Download von Videos
- Dieses Tool ist nur für persönliche Nutzung gedacht
- Manche Videos könnten urheberrechtlich geschützt sein

---

**Viel Spaß mit Ihrem YouTube to MP3 Converter! 🎶**
# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Music is a workspace for audio analysis and music generation tools. Each subdirectory is an independent project with its own setup and dependencies.

## Projects

| Directory | Type | Stack |
|-----------|------|-------|
| `suno-clone/` | Audio analysis pipeline | Python 3.11, librosa, essentia, demucs-mlx |

## suno-clone

Audio analysis pipeline that takes YouTube URLs or local audio files, performs deep feature extraction, and generates Suno v5.5 style-clone prompts. Runs as a Claude Code skill (`/suno-clone`).

See `suno-clone/CLAUDE.md` for full details.

### Commands
```bash
# Setup (first time)
bash suno-clone/scripts/setup.sh

# Activate venv
source ~/.openclaw/envs/suno-clone/bin/activate

# Full analysis pipeline
python suno-clone/scripts/analyze.py "<youtube-url-or-file-path>"
```

## Common Patterns

- **Python venvs:** Managed at `~/.openclaw/envs/<project>/` (not in repo)
- **Audio files:** Excluded from git via `.gitignore` (*.wav, *.flac, *.mp3)
- **Data output:** Stored at `~/.openclaw/data/<project>/` (not in repo)

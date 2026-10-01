# timesage

SSRPG Tool that reads your save and finds the best location to offline farm.

A companion tool for [Stone Story RPG](https://store.steampowered.com/app/1055050/Stone_Story_RPG/)
that reads your save file and figures out the optimal location to farm offline,
for the best enchants or when you can't be bothered to pick a spot yourself.

## Features

- Read and decrypt SSRPG save files.
- Rank locations by completion rate / efficiency.
- Optionally apply active event bonuses (2x chests).
- Copy completion-time tables to your clipboard.
- Includes a web page view.

## Usage

```bash
# CLI
python -m cli.main

# (see app.sh for notes on the web view)
```

Answer the prompts to pick a save file and, if present, apply event bonuses. The
tool prints the best locations and their expected completion times.

## Requirements

```bash
pip install -r requirements.txt
# or use the provided create_venv.sh
```

## Structure

```
cli/         CLI entry points (save loading, output)
core/        save decryption, location data, timewise logic
page/        web view (index.html + timewise.zip)
build_zip.py packs the web view payload
```

> Internal code still references the old name "timewise" / "sundial" in places.

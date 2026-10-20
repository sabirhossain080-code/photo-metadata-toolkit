# Photo Metadata Toolkit

A Python command-line toolkit that scans folders of photographs, extracts
EXIF metadata (date, camera settings, GPS location), and turns it into
structured, analyzable data.

## Features
- Recursively scans folders for JPEG and RAW images
- Extracts date/time, camera, lens, focal length, aperture, shutter speed, ISO, and GPS
- Exports a structured `catalog.csv`
- Generates summary charts (shots per month, focal length and ISO distributions)
- Creates an interactive map of photo locations
- Renames and sorts files by date, with a safe `--dry-run` mode
- Optional GPS rounding to protect sensitive locations

## Motivation
Built from my own wildlife photography workflow, this project turns raw image
metadata into reproducible, analysis-ready data. It demonstrates file
handling, binary metadata parsing, data analysis with pandas, visualization,
and automated testing in Python.

## Installation
    git clone https://github.com/sabirhossain080-code/photo-metadata-toolkit.git
    cd photo-metadata-toolkit
    pip install -r requirements.txt

## Usage
    python -m photometa scan ./photos --out output/
    python -m photometa organize ./photos --dest ./sorted --dry-run
    python -m photometa map output/catalog.csv

## Testing
    pytest

# heic2jpg

Convert a HEIC image to JPEG or PDF from the command line.

## Install dependencies

```sh
python3 -m venv .venv
. .venv/bin/activate
python -m pip install -r requirements.txt
```

## Usage

```sh
./heic2jpg path/to/photo.HEIC
```

By default, the command writes `path/to/photo.jpg`. Use `-p` (or `--pdf`) to write a single-page PDF instead:

```sh
./heic2jpg -p path/to/photo.HEIC
```

This writes `path/to/photo.pdf`. The command prints the output path, leaves the original image unchanged, and does not overwrite an existing output file.

For a single-page PDF under 300 KB (300,000 bytes), use:

```sh
./heic2jpg --pdf-small path/to/photo.HEIC
```

This writes `path/to/photo-small.pdf` without replacing the regular PDF.
It reduces image resolution and JPEG quality as needed. If it cannot meet the
size limit, it reports an error without writing a PDF.

## License

[Apache License 2.0](LICENSE).

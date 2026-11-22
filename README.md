# heic2jpg

Convert a HEIC image to JPEG from the command line.

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

The command writes `path/to/photo.jpg` and prints its path. It leaves the original image unchanged and does not overwrite an existing output file.

## License

[Apache License 2.0](LICENSE).

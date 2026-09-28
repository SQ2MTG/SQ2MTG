# dymoprint

Linux software for printing labels with Dymo LabelManager-class devices.

## Capabilities

The current README documents:

* text printing;
* QR-code printing;
* barcode printing;
* image printing;
* combinations of these elements;
* a PyQt6 GUI with live preview and node-based layout.

Experimental device support includes several LabelManager/LabelPoint models and Windows operation through WinUSB.

## Installation

Recommended installation uses pipx:

```bash
pipx install dymoprint
```

On Debian/Ubuntu, pipx can be installed with:

```bash
sudo apt-get install pipx
```

The application may require a udev rule so the user can access the USB device.

## CLI examples

```bash
dymoprint "Hello world"
dymoprint -qr "QR Content" "Cleartext printed"
dymoprint -c code128 "Test"
dymoprint -p mypic.jpg ""
```

Use `dymoprint --help` for the complete command-line interface.

## GUI

Start the graphical interface with:

```bash
dymoprint_gui
```

The GUI supports text, QR, barcode and image nodes, preview, font selection/scaling, margins and drag-and-drop node ordering.

## Configuration

Fonts are configured through `dymoprint.ini`, normally under `~/.config`.

## Development

Editable installation:

```bash
pip install --editable .
pre-commit install
```

The repository is derived from the historical `computerlyrik/dymoprint` project; current upstream maintenance should be checked before contributing or redistributing changes.

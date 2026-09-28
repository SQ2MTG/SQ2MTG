# dymoprint — Implementation Notes

## Repository provenance

The project descends from the original dymoprint work by Sebastian Bronner and the `computerlyrik/dymoprint` repository. The current README identifies `@maresb` as maintainer.

## Packaging

The documented user installation is via pipx. Development uses an editable Python installation and pre-commit.

## Label composition

The GUI exposes a node model:

* Text Node
* QR Node
* Barcode Node
* Image Node

Nodes can be reordered by drag and drop. The preview reflects margins, font sizing and tape colour schema.

## Hardware boundary

The project targets USB-connected Dymo hardware. The README documents device support and permissions but does not guarantee compatibility for every hardware revision.

## Security note

USB udev rules directly affect device access. Review and scope such rules to the intended device/user rather than blindly copying permissive examples.

## License/provenance

The repository is a fork/derivative of upstream dymoprint. Check the exact license files in the current branch before redistribution or publishing modified binaries.

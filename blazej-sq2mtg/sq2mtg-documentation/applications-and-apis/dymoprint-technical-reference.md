# dymoprint — Technical Reference

## Printing pipeline

dymoprint provides a Linux printing path for compatible Dymo label printers. The user-facing model is:

1. Build a label from text, QR, barcode and/or image content.
2. Render the label to the printer's tape constraints.
3. Send the generated output through the supported USB device interface.

The README explicitly documents CLI and GUI operation; lower-level USB/protocol details should be taken from the implementation rather than inferred.

## Supported content

* Text, including multiline input.
* QR codes.
* Barcodes, including Code 128 examples.
* JPEG images.
* Mixed content.

The GUI represents content as nodes that can be reordered.

## Device support

Primary target: Dymo LabelManager PnP.

Experimental models documented by the project include LabelManager PC, LabelPoint 350, LabelManager 280, LabelManager 420P and LabelManager Wireless PnP.

Windows support is documented through WinUSB/Zadig.

## USB permissions

Generic USB access may require a udev rule. The project prints the required rule guidance on first execution. Treat USB permission rules as security-sensitive: avoid broad `MODE="0666"` rules where a narrower user/group policy is possible.

## Fonts

Font selection is controlled through `dymoprint.ini`. TTF fonts can be selected by path.

## Development validation

The README recommends exercising text, QR and barcode combinations against a real device, not relying solely on CI.

## Known future work

The README lists vertical printing, abstraction refactoring and pixel-font support among remaining work items.

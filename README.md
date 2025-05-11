# QR Code Generator
A JavaScript based qr code generator.

# Fork Disclaimer
This project is a fork of Javascript QR Encoder. It was also released under GPLv3.

Original author's email: tz@execpc.com

# Process

This fork generates the QR in a hidden canvas and converts it into a PNG file via Data URI. It is then inserted into any defined container as an IMG tag. Resize the img tag via CSS as needed.

# Usage

## Adding to Website

Download the JS file and add it to your website or use the URL below.

```
https://cdn.jsdelivr.net/gh/NaeemBolchhi/qrcodegen@main/qr.min.js
```

Or, you can try a script tag with this URL.

```
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/NaeemBolchhi/qrcodegen@main/qr.min.js"></script>
```

Place it at the end of your body tag.

## Function

The function you should call is `doqr()`. It needs to have several variables passed to it.

- doqr(string, ecc, background, foreground, container)
    - `string`: What you want to encode. Should be String.
    - `ecc`: Can be 1, 2, 3, or 4. 1 is Lowest and 4 is Highest. Should be Integer. Check (here)[https://www.han-soft.com/releases/barcode2d/documents/p_ecclevel_qrcode.html] if you want to understand this value.
    - `background`: Background color of the QR. Use a HEX value. Should be String.
    - `foreground`: Foreground color of the QR. Use a HEX value. Should be String.
    - `container`: Point to a document element that will contain the qr. It will be cleaned every time you create a QR. Should be a JS property.

So, here's an example command with all the values inserted:
```
doqr("Example string", 1, "#eee", "#000", document.body);
```

## Test

You can try the code live (here)[https://naeembolchhi.github.io/qrcodegen/test.html].

# License
This project is licensed under GPL v3.0.

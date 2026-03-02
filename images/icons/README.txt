This folder can hold PWA icons. iOS prefers PNGs at multiple sizes (180x180, 152x152, 120x120).

Use ImageMagick to generate PNG icons from the SVG logo, for example:

magick convert images/logo.svg -resize 180x180 images/icons/apple-touch-180.png
magick convert images/logo.svg -resize 192x192 images/icons/icon-192.png
magick convert images/logo.svg -resize 512x512 images/icons/icon-512.png

After generating PNGs, edit `manifest.webmanifest` to reference the PNGs and update the <link rel="apple-touch-icon"> in `index.html` to point to the PNG apple icon.

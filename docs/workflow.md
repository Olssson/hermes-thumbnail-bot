# Local render configuration

Defaults: white background, JPEG quality 92, canvas 1200×1200 px, image box 1080×1080 px (fit only, no upscaling). For another marketplace, change the canvas and image box together. The box must not exceed the canvas. The template pads around an existing image or flattens transparency; it does not detect the product or erase an existing background.

ImageMagick 6 example (use `magick` instead of `convert` on ImageMagick 7). Use simple local names in a new working directory; `input.jpg` must be a product JPEG, and `thumbnail.jpg` must not already exist:

```sh
test -f ./input.jpg && test ! -L ./input.jpg && \
  test ! -e ./thumbnail.jpg && test ! -L ./thumbnail.jpg && \
  convert -limit memory 256MiB -limit map 512MiB -limit disk 512MiB \
    'jpeg:./input.jpg' -auto-orient -colorspace sRGB -resize '1080x1080>' \
    -background white -alpha remove -alpha off -gravity center \
    -extent 1200x1200 -strip -quality 92 'jpeg:./thumbnail.jpg'
```

For PNG input, use `png:./input.png` and update the input checks. Use only trusted images. Review any AI-assisted composition against the actual contents before using it in an offer. Compositions can be prepared outside the agent and imported as files; no authenticated browser automation is included.

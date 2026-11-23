---
name: catalog-thumbnail
description: Prepare a catalog thumbnail from a local product image or review a mockup against its references.
---

# Catalog thumbnail

Use images the operator has permission to process. Keep processing local. Read the output size and background settings in `docs/workflow.md` in the project checkout; defaults are a 1200×1200 white canvas with the product image fitting inside 1080×1080 without enlargement. Use ImageMagick 6 `convert` or ImageMagick 7 `magick`. This does not remove existing opaque backgrounds.

- Use only operator-selected local JPG or PNG inputs. Reject other formats; work on copies under a project-local folder and use simple names such as `input.jpg`. Reject symlinks and paths with shell or ImageMagick metacharacters. Never interpolate raw text into a shell command.
- Apply EXIF orientation, preserve proportions, center the image, strip metadata, and export JPEG for catalog use. Write only a new output file, never overwrite the input or an existing output.
- If a bundle composition is needed, ask the operator for an already composed image or list the reference photos and suggest a composition. Do not imply the local rendering step generates new bundle compositions or replaces the background of an opaque photo.
- Verify output dimensions, compare visible colors, labels and components against the originals, and send the result for human review. Flag differences without inventing specifications. Do not upload to a marketplace.

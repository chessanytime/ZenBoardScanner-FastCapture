# ZenBoardScanner Fast Capture

A separate, lightweight camera tool for taking board photographs after each stable board change.

## What it does

- Opens the camera and lets you auto-detect the board with OpenCV.js.
- Allows manual adjustment of the four board corners.
- Perspective-corrects the complete board into a square image.
- Watches for visual changes, waits until the board is stable, and saves a JPEG.
- Saves JPEGs at 96% quality and bundles the session into a ZIP.
- Optional beep after each saved photo.

## What it deliberately does not do

- No ONNX model download or inference.
- No piece recognition, move identification, legality checks, or PGN generation.
- No connection to the original ZenBoardScanner code or its game-recording workflow.

## Use

1. Open the page over HTTPS (for example, with GitHub Pages) and allow camera access.
2. Start the camera.
3. Auto-detect the board, or drag the four numbered corner markers to the board edges.
4. Lock the corners.
5. Start Fast Capture.
6. Play a move, remove your hand, and wait for the stable board photo to be saved.
7. Download the session ZIP when finished.

You can also use **Capture current board now** for a manual photo.

## Notes

- The first stable frame after starting capture becomes the comparison reference; it is not automatically saved. Each subsequent stable visual change can create a photo.
- Keep hands and other objects clear of the board during the settle period. This tool detects visual change and stability only; it does not understand what caused the change.
- Photos are processed locally in the browser. The ZIP is generated locally and downloaded to your device.
- Camera access requires HTTPS or localhost.

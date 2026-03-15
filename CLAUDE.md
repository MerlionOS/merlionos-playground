# merlionos-playground

Browser-based MerlionOS playground using v86 x86 emulator.

## How It Works

- v86 (JavaScript x86 emulator) boots the MerlionOS bootimage directly in the browser
- No backend needed — pure static HTML + JS
- VGA display rendered to HTML canvas
- Keyboard input forwarded to the virtual machine

## Files

- `index.html` — Single-page playground UI
- `images/merlionos.bin` — Compiled MerlionOS bootimage (floppy disk image)

## Updating the Kernel Image

```bash
cd ../merlion-kernel
make build
cp target/x86_64-unknown-none/debug/bootimage-merlion-kernel.bin \
   ../merlionos-playground/images/merlionos.bin
```

## Deployment

Deployed via GitHub Pages. Push to main triggers automatic deployment.

## URL

- playground.merlionos.org (or merlionos.org/playground)

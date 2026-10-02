# Doom RPG — UAC Field Terminal

Doom RPG (id Software / Fountainhead, 2005, J2ME) running in the browser. The Java game and a
MIDP compatibility layer are ahead-of-time compiled to JavaScript with TeaVM, then packaged with
every game resource into a single HTML file.

| Path | What it is |
| --- | --- |
| `site/index.html` | The playable build, served at the root of the Pages site |
| `site/architecture.html` | A technical write-up of the engine: MIDP bridge, software framebuffer, input, MIDI → Web Audio synth, RecordStore persistence, TeaVM threading |
| `.github/workflows/pages.yml` | Deploys `site/` to GitHub Pages |

## Controls

Arrows / WASD move and turn · Enter or Space to act · Q menu · E map · Z / X strafe · 0–9, `*`, `#` act
as the phone keypad. On touch devices, use the on-screen keys. Saves are stored in the browser's
`localStorage`.

## Deploying

The workflow runs on every push to `main` that touches `site/`, and you can also run it by hand from
the Actions tab. You only need to set this up once: **Settings → Pages → Build and deployment →
Source: GitHub Actions**.

To run it locally, open `site/index.html` directly, or serve the folder:

```sh
python3 -m http.server -d site
```

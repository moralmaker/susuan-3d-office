# SuSuan 3D office P0.1

This is the SuSuan 3D office P0.1 Three.js walkthrough: a static first-person WebGL scene (Pointer Lock + WASD) of 素算科技开放式办公场景. No backend, no login, and no private business data.

## Live

https://moralmaker.github.io/susuan-3d-office/

## Local

Open `index.html` in a modern browser, or serve this directory:

```bash
python3 -m http.server 8765
```

Three.js `0.160.0` loads from jsDelivr. Wall and plaque files use relative paths under `assets/`.

## Controls

| Action | Result |
|--------|--------|
| Click「进入场景」 | Pointer Lock, first person |
| WASD / arrow keys | Move |
| Mouse | Look around |
| Esc | Release the pointer |
| Click the crosshair | Open a zone, plaza, or culture-wall panel |
| Top bar「俯视/轨道」 | Orbit overview |
| 「文化墙」 | Brand copy |

## Files

- `index.html` — Three.js walkthrough
- `assets/wall/` — culture-wall textures
- `assets/plaques/` — zone plaques
- `验收清单.md` — P0.1 checklist

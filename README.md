# SuSuan 3D office P0.2 M1

This is the SuSuan 3D office walkthrough: a static first-person WebGL scene (Pointer Lock + WASD) of 素算科技开放式办公场景. No backend, no login, and no private business data.

## 本轮范围（P0.2 M1）

本轮：通透开放布局；材质/家具仍为程序化占位，非孪生级；非影视扫描重建。

各中心不再使用半高隔断或房间盒子。分区靠地面色带、地毯色块、区牌和矮工位岛表示，站立视线可以穿过整个楼层。文化墙贴图源、文案和 3:4（1200×1600）比例未改；立面朝向广场，默认出生点在广场北侧、面向文化墙正面。PBR 材质库和 GLTF 家具不在本轮。

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
- `验收清单.md` — P0.1 checklist（其中「半高墙 / 工区体块」已被本轮通透布局取代）

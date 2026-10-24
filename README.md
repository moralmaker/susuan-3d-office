# SuSuan 3D office P0.2

素算科技开放式办公的静态第一人称 WebGL 场景（Pointer Lock + WASD）。无后端、无登录、无私人业务数据。

## 本轮范围（P0.2 孪生观感）

本轮：通透布局 + PBR/灯光 + 开源 GLTF 家具；实时 WebGL 孪生观感；非影视级扫描重建。

各中心没有高隔断。分区靠地面色带、地毯、区牌和矮工位岛表示，眼高 1.65m 可以越过桌椅（桌面约 0.75m）看到整个楼层。文化墙贴图源、文案和 3:4（1200×1600）contain 未改；默认出生点在广场北侧，面向文化墙南立面。

## Live

https://moralmaker.github.io/susuan-3d-office/

## Local

用现代浏览器打开 `index.html`，或在本目录起静态服务（GLTF 需要 http，不要用 `file://`）：

```bash
python3 -m http.server 8765
```

Three.js `0.160.0` 从 jsDelivr 加载。墙面、区牌、家具使用 `assets/` 下的相对路径。

## Controls

| Action | Result |
|--------|--------|
| Click「进入场景」 | Pointer Lock, first person |
| WASD / arrow keys | Move |
| Mouse | Look around, pitch ±70° |
| Esc | Release the pointer |
| Click the crosshair | Open a zone, plaza, or culture-wall panel |
| Top bar「俯视/轨道」 | Orbit overview |
| 「文化墙」 | Brand copy |

## 模型与授权

家具几何只下载一份，工位岛用 clone 共享。整套 GLB 约 1.1MB。

| 文件 | 角色 | 来源 | 授权 |
|------|------|------|------|
| `assets/models/desk.glb` | 工位桌 / 共享桌 | MrEliptik《Office low poly pack》`desk_big` | CC0 |
| `assets/models/chair.glb` | 办公椅 | 同上 `office_chair` | CC0 |
| `assets/models/monitor.glb` | 显示器机身 | 同上 `monitor`（屏面为场景内发光片，便于识别） | CC0 |
| `assets/models/lamp.glb` | 台灯 | 同上 `lamp` | CC0 |
| `assets/models/mouse.glb` | 鼠标 | 同上 `wireless_mouse` | CC0 |
| `assets/models/keyboard.glb` | 键盘 | Kenney Furniture Kit `computerKeyboard` | CC0 |
| `assets/models/cabinet.glb` | 矮柜 | Kenney Furniture Kit `sideTableDrawers` | CC0 |
| `assets/models/houseplant.glb` | 落地绿植 | Quaternius Ultimate House Interior `Houseplant_6` | CC0 |
| `assets/models/houseplant-small.glb` | 柜上绿植 | Quaternius 同上 `Houseplant_3` | CC0 |

MrEliptik 键盘单体约 8MB 高模键帽，未打进页面，改用 Kenney CC0 键盘。Poly Pizza 直链被 CDN 拦截，绿植改用同一 Quaternius CC0 室内包里的 Houseplant。未使用 Sketchfab NC，也未使用 Poly Haven 4k。

## Files

- `index.html` — Three.js walkthrough
- `assets/wall/` — culture-wall textures（本轮未改）
- `assets/plaques/` — zone plaques（本轮未改）
- `assets/models/` — CC0 GLB furniture
- `验收清单.md` — P0.1 checklist（其中「半高墙 / 工区体块」已被通透布局取代）

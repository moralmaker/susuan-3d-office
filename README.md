# 素算 · 开放总部沙盘

素算科技开放式总部的静态 WebGL 场景（步行 + 环绕 + 俯瞰）。无后端、无登录、无私人业务数据。

## 本轮范围（HQ 级实时沙盘）

逼真度边界：对标 HQ 级实时 WebGL 总部沙盘观感（回字开放总部、中央核心、PBR 光影与视角切换）。非影视扫描重建；未复制 [agent-display](https://github.com/cyberdaddyleo/agent-display) 源码（该仓为 PolyForm Noncommercial，本实现为自研几何、材质与布局）。

各中心没有高隔断。回字楼板把中央核心（会议长桌 + 开放领导岛）和四周中心簇分开，分区靠石材走道、编织地毯、簇色细框和区牌表示。眼高 1.65m 可以越过桌椅（桌面约 0.75m）看到整个楼层。文化墙贴图源、文案和 3:4（1200×1600）contain 未改；默认出生点在广场北侧，面向文化墙南立面。

帧率持续低于约 28fps 时会自动降到均衡（关辉光、阴影 1024）或流畅（关阴影）。可用 `?cam=walk|orbit|top` 直接进入对应视角，`?shot=1` 跳过点击进入，便于截图。

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
| `1` / `2` / `3` | 步行 / 环绕 / 俯瞰 |
| Top bar | Same three cameras; 环绕 idles into a slow turn |
| Click the crosshair | Open a zone, plaza, or culture-wall panel |
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

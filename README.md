# PokePic

宝可梦贴图浏览器。**图片直连公有 CDN**，仓库里只放 Café ReMix 那套（源站有 Cloudflare，没法 hotlink）。

👉 <https://sgorgeous.github.io/pokemon-sprite/>

## 两套界面，自动分流

| 入口 | 说明 |
|---|---|
| `/`（index.html） | 路由：手机/窄屏 → `mobile.html`，桌面 → `desktop.html` |
| `/mobile.html` | **PokePic 手机版**：底部五页签、长按多选、缓存、收藏、存相册、中文搜索、PMD 表情、左右滑动看图 |
| `/desktop.html` | 原桌面版：左侧系列栏 + 顶部页签 |
| `/update.json` | App 更新清单（App 启动时读） |

强制指定：`?ui=m` 手机版 / `?ui=d` 电脑版。

## 素材来源

| 页签 | 来源 |
|---|---|
| 图鉴（Showdown） | `play.pokemonshowdown.com/sprites/` |
| 迷宫（PMD） | GitHub `PMDCollab/SpriteCollab`（raw / fastly / jsDelivr 自动换源） |
| 咖啡厅（Café） | **本仓库** `PokemonCafeRemix/`（1875 张） |
| 收藏 / 缓存 | 浏览器 IndexedDB |

`PokemonShowdown/` `PokemonMysteryDungeon/` `PokemonOfficialArtwork/` 三个目录是空的，图片走 CDN。

## 说明

- 素材版权归 The Pokémon Company，仅供个人查阅与研究。作者 **ACMinerva**。
- 手机版与安卓 App 是同一份页面；App 源码在本地 `D:\WorkStation\deepseek\works\pokepic\`，
  改完跑 `tools\sync_web.py --deploy` 同步到这里。

# PokémonSprite 在线阅读器

宝可梦贴图浏览器。**页面只带索引，图片从公有 CDN 直连**，仓库里只放 Café ReMix 那套
（因为它源站有 Cloudflare，没法 hotlink）。

👉 打开：<https://sgorgeous.github.io/pokemon-sprite/>

## 四个页签，图从哪来

| 页签 | 图片来源 | 说明 |
|---|---|---|
| **Showdown** | `play.pokemonshowdown.com/sprites/` | 61 个子目录（各世代精灵图 / 动态 GIF / HOME 渲染 / 图标 / 训练家），约 5.3 万个 |
| **PMD 动画** | `raw.githubusercontent.com/PMDCollab/SpriteCollab` | 不可思议迷宫 Q 版，1026 只 / 4460 形态；序列帧 + `AnimData.xml` 现场拉，Canvas 抽帧播放 |
| **官方立绘** | `raw.githubusercontent.com/PokeAPI/sprites` | 1351 条（1025 图鉴 + 全部形态）× 官方设定画 / HOME 渲染 / 异色 |
| **Café ReMix** | **本仓库** `PokemonCafeRemix/` | 1875 张（1263 立绘 + 612 头像），源站 Bulbagarden 有 Cloudflare 拦 `<img>`，只能自托管 |

`PokemonShowdown/`、`PokemonMysteryDungeon/`、`PokemonOfficialArtwork/` 三个目录是空的，
图片由 CDN 提供，不需要进仓库。

## 用法

- 直接开网页；顶部搜索框**跨全部系列**按名字查（`pikachu` 会同时命中 50 个系列/目录）
- 右上角「源」可在 GitHub raw / jsDelivr(fastly) 之间切换（国内 jsDelivr 主域连不上）
- PMD 页签：选宝可梦 → 形态 → 动作 → 朝向；空格播放，←→ 换朝向，↑↓ 换动作

## 数据

`data/` 里是索引（1.1 MB）：61 份 Showdown 名单、`names.json`（名字→系列映射）、
`pmd.json`（物种→形态→仓库路径）、`official.json`（PokeAPI 图鉴表）。

## 说明

- 素材版权归 The Pokémon Company 所有，这里仅供个人查阅与研究。
- 图片直连别人的服务器，不缓存、不代理；人多了可能被限流。
- 自建索引与页面：本地库 `Q:\文件\素材\PokemonSprite\_tools\`（不随此仓库发布）。

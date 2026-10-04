<div align="center">
  <img src="media/ae2b496c-dd39-4440-b835-8502c06769c2.png" width="420" alt="可搜网易云" />
</div>

<h1 align="center">可搜网易云</h1>

<p align="center"><em>给小米手表上的网易云音乐（Vela 快应用）加装歌曲搜索</em></p>

<p align="center">
  搜歌名 / 歌手 / 关键词　·　点进结果直接播放　·　可下载到「本地歌曲」离线听　·　键盘带 123 数字页
</p>

---

本仓库是 **AstroBox 资源仓库**，只放打包好的 `.rpk` 与资源索引 `manifest_v2.json`。
源码、构建方法、完整技术报告（为什么云端收藏不了、双 id 空间是怎么回事……）在：
**[Cookie-Zalea/netease-vela-search](https://github.com/Cookie-Zalea/netease-vela-search)**

## 安装

在 AstroBox 里打开资源页安装：

**https://abox.run/open?source=resv2&id=io.github.cookiezalea.velasearch&provider=OfficialV2**

也可以直接下载下表里的 `.rpk`，用 AstroBox / adb 装到手表。

## 两个版本：正式版 / 试用版

内容一字不差（v1.0.58），**只有包名不同**，按需选一个装：

| | 正式版 | 试用版 |
|---|---|---|
| 包名 | `io.github.cookiezalea.velasearch` | `com.netease.vela`（原版包名） |
| 文件 | [`downloads/io.github.cookiezalea.velasearch.1.0.58.rpk`](downloads/io.github.cookiezalea.velasearch.1.0.58.rpk) | [`downloads/trial/com.search.1.0.58.rpk`](downloads/trial/com.search.1.0.58.rpk) |
| 装上去 | 表里多一个**新应用**，与原版网易云并存 | **直接覆盖原版网易云** |
| 登录 / 已下载的歌 | 都要重来（新包是另一个应用） | **原样保留** |
| 适合 | 想保留原版，让搜索版独立存在 | 不想重新登录、想无缝升级 |

> ⚠️ 试用版会覆盖官方 App（官方后续更新、卸载都会把它带走），介意就用正式版。
> 装过 1.0.57 的（无论哪个版本），都可直接覆盖升级到 1.0.58 —— 同包名、内容也一致，只是换了编译模式。

## 版本

| 版本 | 说明 |
|---|---|
| **1.0.58**（当前） | 内容与 1.0.57 相同，改用 release（生产模式）编译，搜索页 JS 334KB → 181KB；正式 / 试用双轨齐全 |
| 1.0.57 | 包名从 `com.netease.vela` 改为 `io.github.cookiezalea.velasearch`（反 DNS 命名）；修「真机键盘一行只显示七个字母」（容器宽度写死 480） |
| 更早 | `1.0.52`（新增搜索下载）起，各版本仍留在 `downloads/` 里留档 |

## 说明

- 键盘组件来自 [NEORUAA/Vela_input_method](https://github.com/NEORUAA/Vela_input_method)（MIT 许可）。
- **搜索到的歌云端收藏不了**（平台限制：公开接口的数字 id 与 app 的 32 位 hex id 互不相认）。
  点心形会弹一句实话提示、心形不翻；播放、下载、离线收听都不受影响。
  原版入口（每日推荐 / 私人 FM / 我喜欢 / 本地歌曲）的收藏**不受影响**。
- 更多细节与已知限制见主仓库的 README。
- 本项目与网易、小米均无关联，是个人学习性质的改包，请勿用于商业用途。

---

如果它让你在手表上听歌方便了一点，欢迎到主仓库点个 ⭐，有问题也欢迎提 Issue。

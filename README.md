# 网易云音乐 · MyGo Music 插件

适用于新版 [MyGo Music](https://github.com/egoist/mygo-music) 的个人使用插件。运行于宿主的 moejs，不需要 Node、代理 API 服务或启动外部程序。目标宿主：MyGo Music 0.1.6。

## 安装和使用

1. 打开 MyGo Music → 设置 → 插件 → `+` → 从 GitHub 安装，填入 `sogud/mygo-music-netease`。也可从 [Releases](https://github.com/sogud/mygo-music-netease/releases) 下载 ZIP 后从本地安装，或选择本项目文件夹。
2. 核对插件仅请求 `music.163.com`、`interfacepc.music.163.com` 网络权限，确认安装。
3. 在来源选择器中选择 **网易云音乐**。未登录也可搜索、浏览推荐歌单和排行榜、播放平台允许的完整曲目。
4. 点击 **登录**，用网易云音乐手机 App 扫码并确认，读取自己的歌单和喜欢的音乐。请勿把二维码或 Cookie 发到聊天中。

如果手动复制插件：通过宿主“显示插件文件夹”找到目录，把 `plugin.json`、`index.js`、`LICENSE`、`THIRD_PARTY_NOTICES.md`、`README.md` 放在其 `netease/` 子目录，重启宿主。

## 功能

- 歌曲、专辑、歌手、歌单搜索，支持翻页。
- 推荐歌单、排行榜、歌单详情，专辑和歌手详情。
- 网易云 App 扫码登录、会话恢复、个人歌单、喜欢列表、喜欢/取消喜欢。
- 标准/高音质/无损请求，按当前账号的实际权限返回音频。
- LRC 歌词和翻译，交给 MyGo Music 原生播放界面显示。

不返回 VIP 试听片段作为完整歌曲，不解锁付费内容，也不从其他音乐来源替换歌曲。无权限、地区受限、下架或平台不返回地址时会明确报错。

首版每个歌单最多载入 1000 首，超过时在歌单说明中提示；歌手页显示热门歌曲和最新 30 张专辑。暂不提供歌单编辑、评论、播客、逐字歌词及每日推荐歌曲。喜欢/取消喜欢只在用户点击相应按钮时发送。

## 会话与权限

只通过网易云官方域名发起请求。Cookie 不发送到音频 CDN，不记录到日志，也没有手动粘贴 Cookie 的设置项。

宿主把登录会话保存在自己的 `plugin-data/netease/storage.json`，目录权限为 `0700`，文件权限为 `0600`。这是宿主提供的本地 JSON 存储，并非系统钥匙串；请勿分享这个文件。退出登录会删除本插件的会话，不影响其他网易云客户端。

## 开发

运行不需要构建或依赖安装；Node 和 Python 仅用于本地检查及打包：

```sh
npm run check
npm test
npm run pack
```

`index.test.mjs` 使用 Node 自带测试框架和虚构会话；真实宿主验证使用上游 `internal/plugin` 的加载器和 moejs。模块顶层不调用 `host.storage`，以兼容 0.1.6 的加载锁。

## 来源与限制

请求协议和数据转换移植自 [sogud/mygo-cloudmusic](https://github.com/sogud/mygo-cloudmusic)，来源与改动见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。许可为 [AGPL-3.0](LICENSE)。

这是非官方插件。旧客户端上游曾因网易云要求而下线；接口、服务条款及分发限制可能变化，本项目不保证持续可用。源码与安装包遵循 AGPL-3.0 提供，音乐内容和服务访问权不属于本项目的许可范围。

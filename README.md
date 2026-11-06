# 网易云音乐 · MyGo Music 插件

在 [MyGo Music](https://github.com/egoist/mygo-music) 中搜索和播放网易云音乐。支持 MyGo Music 0.1.6，无需额外服务。

## 安装和使用

1. 打开 MyGo Music → 设置 → 插件 → `+` → 从 GitHub 安装，填入 `sogud/mygo-music-netease`。也可从 [Releases](https://github.com/sogud/mygo-music-netease/releases) 下载 ZIP 后从本地安装，或选择本项目文件夹。
2. 安装后，在来源选择器中选择 **网易云音乐**。
3. 点击 **登录**，用网易云音乐手机 App 扫码，访问自己的歌单和喜欢的音乐。

## 功能

- 歌曲、专辑、歌手、歌单搜索，支持翻页。
- 推荐歌单、排行榜、歌单详情，专辑和歌手详情。
- 登录后的每日推荐、私人雷达、个性化歌单，以及持续补充歌曲的私人漫游、熟悉的歌和新发现。
- 网易云 App 扫码登录、会话恢复、个人歌单、喜欢列表、喜欢/取消喜欢。
- 标准、高音质和无损音质。
- LRC 歌词和翻译，交给 MyGo Music 原生播放界面显示。

## 开发

运行不需要构建或依赖安装；Node 和 Python 仅用于本地检查及打包：

```sh
npm run check
npm test
npm run pack
```

[AGPL-3.0](LICENSE)

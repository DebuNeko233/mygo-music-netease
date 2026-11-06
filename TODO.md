# TODO

- [x] 2026-11-06 14:53 UTC · Codex（ChatGPT 委派 / Mac mini）· 按用户后续要求公开发布 `sogud/mygo-music-netease` 与 `v0.1.0` ZIP；按用户要求简化 `README.md` 和 Release 说明，移除“来源与限制”章节。保留许可证及独立署名文件。

- [x] 2026-11-06 14:47 UTC · Codex（ChatGPT 委派 / Mac mini）· 新增 `index.js`、`plugin.json`，移植搜索、歌单、歌词、扫码登录、喜欢列表及授权播放；新增 `index.test.mjs`、`pack.py`、README、AGPL 许可和来源说明。8 项测试及上游 `internal/plugin` 测试通过；真实 moejs 验证四类搜索、24 推荐歌单、65 榜单、59 首歌单、歌词、专辑、歌手 50 首/30 专辑、扫码生成及 HTTP 206 音频解码（48000 Hz）。
- [x] 2026-11-06 14:47 UTC · Codex（ChatGPT 委派 / Mac mini）· 官方 MyGo Music 0.1.6 已安装到 `/Applications/MyGo Music.app`，SHA-256 与官方发布值一致，签名和公证通过；插件 ZIP 通过宿主安装器安装到 `~/Library/Application Support/MyGo Music/plugins/netease/`，原生界面已显示推荐歌单和搜索结果。
- [ ] 2026-11-06 14:47 UTC · Codex（ChatGPT 委派 / Mac mini）· 用户扫码后的个人歌单、真实喜欢操作、VIP/无损播放权限和重启后的真实会话恢复仍需账号验收；未读取已有其他客户端凭据，未进行真实喜欢/取消喜欢写操作。

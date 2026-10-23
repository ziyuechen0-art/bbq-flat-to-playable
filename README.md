# bbq-flat-to-playable

`v0.1.0-beta` 公开试用版。将已有烧烤三消平面 PSD 整理为可玩美术交付。Photoshop 实际执行及跨电脑测试尚未完成；不代表已制作可运行广告。

完整规范见 [SKILL.md](skills/bbq-flat-to-playable/SKILL.md)。Photoshop 执行注意事项已内联，无外部案例或随包脚本依赖。

## 默认交付

- 两套 720×1280 竖版玩法 PSD、一份 720×1280 胜败结束页 PSD、一份 1280×720 双皮肤横版 PSD。
- 6 张带批注 PNG：横版两张、竖版两张、胜利和失败各一张。实际素材由使用者提供，仓库不包含这些交付文件。
- 两套竖版玩法及结束页的非文字内容层栅格化，保留独立素材和分组；文字保持可编辑。横版不默认强制全部栅格化。
- 图层及组使用有意义的英文字母命名。横竖及胜败页面统一按钮；btn 为无字底图，playnow 为独立可编辑 PLAY NOW 文字层。
- 批注仅写实际状态、样式与必要数值；保留备份、横竖适配、导出读回及逐项验收要求。盘数、布局及比例遵循当次任务。

## Codex 安装

在 Codex 输入：

```text
$skill-installer 请从 https://github.com/ziyuechen0-art/bbq-flat-to-playable/tree/v0.1.0-beta/skills/bbq-flat-to-playable 安装此 Skill。
```

公开仓库可匿名下载，无需 GitHub 账号、令牌或 GitHub CLI 登录。安装成功后下一轮调用；若未发现则重启 Codex。安装位置由本机 skill-installer 决定。

也可无需 GitHub 账号手动安装：下载 [Beta ZIP](https://github.com/ziyuechen0-art/bbq-flat-to-playable/archive/refs/tags/v0.1.0-beta.zip)，解压后将 `skills/bbq-flat-to-playable` 文件夹放入用户目录的 `.agents/skills/`，确保最终为 `~/.agents/skills/bbq-flat-to-playable/SKILL.md`（Windows 为 `%USERPROFILE%\.agents\skills\bbq-flat-to-playable\SKILL.md`）。不要复制整个仓库作为 Skill 文件夹。

同名 Skill 已存在时先备份到 Codex 不扫描的位置，再移出旧安装目录并安装新标签；避免在多个扫描位置重复安装。安装副本不会自动同步 GitHub，不随更新覆盖 Photoshop 插件或个人配置。

参考：[OpenAI 官方 Skill 文档](https://developers.openai.com/codex/skills/)。

## Photoshop 依赖与首次使用

1. 安装并启动合法可用的 Adobe Photoshop。配置团队认可、可用的 Photoshop MCP 或等价脚本执行通道；本仓库不附带或自动安装插件、服务器、字体或个人配置。
2. 在 Codex 只读核对连接、目标文档、层树及预览。在授权测试副本验证图层操作、栅格化、可编辑文字、另存 PSD、导出 PNG 与重新打开能力。发现工具名称不代表连接或功能验证成功。
3. 提供有使用权限的源 PSD、需求正文、必要字体及独立输出目录。原始文件只读；修改已有交付前备份，保留未保存编辑。
4. 按 Skill 逐项验收。字体缺失时明确报告，不猜测或静默替换。Python 与 psd-tools 仅为可选只读分析工具，不是必装依赖。

```text
$bbq-flat-to-playable 使用我提供的最新平面 PSD 和本次可玩需求，输出到独立目录。
按 Skill 完整规范制作、备份、导出并验收；盘数与布局按本次需求，不套用历史案例。
```

没有可用 Photoshop 执行通道时，只能分析需求和提供操作指导，不能声称自动编辑或交付验证已完成。

## Beta 验收状态

- 本次发布仅核对文档格式、完整性、依赖及公开文件范围。
- Photoshop 实际执行尚未完成，包括图层栅格化、按钮分层、横竖及胜败一致性、批注参数、保存重开与 6 张 PNG 验收。
- 跨电脑安装、环境配置及完整流程测试尚未完成。
- 首次试用使用授权测试副本，逐项记录通过、失败或未执行，不把文档检查当成功能验收。

## 共享范围

仅公开 README.md、.gitignore、skills/bbq-flat-to-playable/SKILL.md 三个文件中的通用指令。无公司具体项目内容、历史案例、原始素材路径、PSD、图片、缓存、凭据或个人配置。素材与字体由使用者自行提供，本仓库不授予任何第三方素材再分发权限。

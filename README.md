# 拾光 · 情绪日记与自我关怀

面向年轻人的情绪记录与自我关怀网页雏形。通过小猫、小狗或小鸟伙伴的对话记录情绪，查看每日变化，获得舒缓建议与成长奖励。

在线作品：https://mood-care-journal.plucky-teal-5337.chatgpt.site

## 当前实现

- 通过自然语言对话归纳情绪、强度和触发情境，由用户确认或纠正。
- 采用浏览器内的规则分析，尚未接入外部大模型，也不需要 API Key。
- 提供七日情绪轨迹、日记回看、JSON 导出、记录删除、呼吸练习和关怀建议。
- 可选择猫、狗、鸟；平静或愉快的不同日期累计为晴心日，达到 3 天、7 天时进化。宠物暂用图标展示。
- 情绪文字和记录仅保存在当前浏览器的 localStorage，不会随 GitHub 或账号自动同步。

## 在另一台电脑继续开发

1. 克隆本仓库，或在 GitHub 点击 Code → Download ZIP 并解压。
2. 用编辑器或 Codex 打开项目根目录，先阅读本文件和 `AGENTS.md`。
3. 直接修改根目录 `index.html`。这是单页静态应用，没有 npm 依赖或构建步骤。
4. 推荐通过本地 HTTP 服务预览。安装 Python 后，在项目目录运行：

```powershell
py -m http.server 8000
```

打开 `http://localhost:8000`。macOS/Linux 可将 `py` 换成 `python3`。

发布前，把最新源文件复制到静态发布目录：

```powershell
Copy-Item .\index.html .\dist\index.html -Force
```

macOS/Linux 对应命令为 `cp index.html dist/index.html`。

## 继续发布到同一个域名

现有作品使用 Sites 托管。`.openai/hosting.json` 已保留原站点身份：

- project_id：`appgprj_6ae0630dbf94819190adf277e57f62cc`
- static.directory：`dist`
- 固定域名：`mood-care-journal.plucky-teal-5337.chatgpt.site`

在另一台电脑登录拥有该站点的同一账号，并使用 Sites 插件继续发布此项目。让编码助手读取 `.openai/hosting.json`，按照 Sites 技能流程同步源代码、保存版本、部署并确认公开访问。必须复用原 project_id，不要新建站点或修改 slug/域名。

GitHub 保存的是源码备份；提交 GitHub 不会自动更新当前在线作品。Sites 的源仓库和 GitHub 仓库是两个发布目的地，发布时应保留历史并按正常流程处理同步，不能强推覆盖。

首次上线对应源提交：`171623c868a33783605f2f460649001deb512594`。

## 给下一次开发对话的交接提示

> 请继续开发“拾光”情绪日记项目。先阅读 README.md、AGENTS.md 和 .openai/hosting.json。当前是无依赖的 HTML/CSS/JavaScript 单页应用，根目录 index.html 是源文件，dist/index.html 是发布副本。继续完善萌宠对话采集情绪、及时安抚、每日情绪追溯和晴心日进化奖励。当前规则分析尚未接入外部大模型。所有发布必须复用现有 Sites project_id 和固定域名，并保持公开访问。不要上传用户日记、密钥或浏览器数据。

## 数据与边界

换机开发可以从仓库恢复全部源码；原浏览器中的个人情绪记录不会自动迁移。当前支持 JSON 导出，尚未实现导入与跨设备同步。公开仓库只包含应用源码、示例内容和交接文档。

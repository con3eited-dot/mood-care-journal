# Project handoff

- 产品名：拾光 · 情绪日记与自我关怀。主要语言为简体中文。
- 根目录 `index.html` 是源文件；`dist/index.html` 是发布副本。修改页面后同步副本。
- 项目是无 npm 依赖的静态单页应用。情绪分析目前为本地规则，不应声称已经接入外部大模型。
- 保留萌宠对话采集、安抚建议、情绪追溯、晴心日成长与进化、勋章功能。宠物暂用图标，不必制作具体角色造型。
- 情绪记录存储在浏览器 localStorage；不得上传真实用户日记或浏览器数据。
- Sites project_id 必须保持为 `appgprj_6ae0630dbf94819190adf277e57f62cc`。
- 固定线上域名为 `mood-care-journal.plucky-teal-5337.chatgpt.site`。继续发布必须复用 `.openai/hosting.json`，不得新建站点或修改 slug/域名，并确认公开访问。
- GitHub 源码提交不会自动部署 Sites。两者 Git 历史独立；发布时先用 Sites 技能在另一空目录恢复原站点源仓库，再复制更新的页面与文档，在该 Sites 工作目录中走正式流程。不要直接把 GitHub 克隆目录的历史推到 Sites，不得强推或覆盖远端历史。
- 不提交密钥、临时凭证、个人日记导出、机器专属配置或依赖目录。

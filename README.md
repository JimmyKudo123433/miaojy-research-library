# Miaojy Research Library

围绕**复杂越野环境下 Segway 式智能无人小车的横向稳定控制**，持续整理两轮自平衡、侧倾控制、地形适应、轮地接触与抗滑研究。

网站：[Miaojy Research Library](https://jimmykudo123433.github.io/miaojy-research-library/)

## 研究资料

- **Paper Pool**：可搜索并按主题、来源、年份、相关度筛选论文。
- **Daily Archive**：查看每日推荐和历史条目。
- **Quick Read**：快速了解问题、方法、结果与研究价值。
- **论文详情**：查看研究动机、方法、证据化贡献、研究问题、实验结果、局限、与本课题的联系和后续研究建议。
- **阅读状态与个人笔记**：收藏、标记阅读进度并维护本地个人状态；公共站点默认只读。

目前已导入 5 篇种子论文。两篇来源目前仅核实到摘要，详情会明确说明证据范围；其余论文依据可访问的全文/官方 HTML 整理。排名未核实时不作推断。

## 研究配置和数据

- `config/research-profile.yaml`：研究方向、主题、摘要语言、每日推荐频率与时区。
- `data/papers/`：论文元数据、Quick Read 和详细报告。
- `data/daily/`：每日推荐归档。
- `data/user/`：阅读状态、收藏、个人标签和笔记。
- `prompts/miaojy-scheduled-task.md`：可绑定本仓库的每日研究任务提示词。

每日研究任务提示词已经按本仓库生成。若希望自动更新论文池，在 ChatGPT 的 Scheduled 中创建每日 08:00（Asia/Shanghai）任务，并把该文件内容作为任务指令；授权连接 `JimmyKudo123433/miaojy-research-library` 的 Contents 读写权限。网站由 GitHub Actions 自动构建并部署，部署工作流会先校验论文数据和构建结果。

## 本地预览

```bash
npm ci
npm run dev
```

更新论文数据后运行 `npm run validate:data`，再提交并推送到 `main`。GitHub Pages 通过 `.github/workflows/pages.yml` 发布。

此网站使用 [research-library-template](https://github.com/kangkang03jug/research-library-template) 创建。编辑器后端未配置时，公开网站保持只读；不要把 GitHub token、App 密钥或其他秘密提交到仓库。

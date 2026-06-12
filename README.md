# Agent Skills 总览

所有自定义 / 第三方 Agent Skills 的唯一 source of truth。按「集合 + 类型」分层存储，集合永不拆散。

## 管理规则

- 仓库本体在 `D:\code\mine\agent-skills`（本仓）；Codex 运行时目录 `C:\Users\admin\.codex\skills\<name>` 仅放 junction 挂载。
- 启用 skill = 建 junction：`mklink /J C:\Users\admin\.codex\skills\<name> <仓库内路径>`；停用 = 删除该 junction，仓库内容不动。
- 组件库（如 react-bits）是项目实现素材，不是 skill，不进本仓，只在「外部参考」登记。
- 个人数据不入仓：`collections/create-yourself/selves/` 已 gitignore。
- 引入外部 skill 前先做安全审查，结论记入 knowledge-base（global/personal-brain/references/agent-skills-and-frontend-libraries）。
- 2026-06-12: taste-skill 仅保留现行 v2（design-taste-frontend），v1 已移除。

## 参考 `reference/`

仅收藏快照、不挂运行时（Codex 扫描不到）。每个快照附 `SNAPSHOT.md` 记录上游 commit 与裁剪说明。

## 集合 `collections/`

| 集合 | 数量 | 状态 | 说明 |
| --- | --- | --- | --- |
| `superpowers/` | 14 | ✅ 在用 | 工程方法集：头脑风暴、写计划、TDD、系统化调试、验证后交付、代码审查等 |
| `understand-anything/` | 8 | ✅ 在用 | 项目理解集：代码库知识图谱、diff 分析、领域提取、上手指南 |
| `create-yourself/` | 1 | ✅ 在用 | 数字分身集：聊天记录/日记/照片蒸馏为可运行人格（selves/ 个人数据不入仓） |

### superpowers 明细

| Skill | 用途 |
| --- | --- |
| `using-superpowers` | 会话起点协议：回应任何请求前先查找并加载合适的 skill |
| `brainstorming` | 动手开发前先探索用户意图、需求和设计方案 |
| `writing-plans` | 拿到需求后先写多步实现计划，再碰代码 |
| `executing-plans` | 按已写好的实现计划分阶段执行，带审查检查点 |
| `test-driven-development` | 实现功能或修 bug 前先写测试（TDD） |
| `systematic-debugging` | 遇到 bug / 测试失败时先系统化定位根因，再提修复 |
| `verification-before-completion` | 声称"完成/修好/通过"之前必须先跑验证命令拿证据 |
| `requesting-code-review` | 完成任务或合并前请求代码审查，核对是否满足需求 |
| `receiving-code-review` | 收到审查意见后先技术验证再实施，不盲从 |
| `dispatching-parallel-agents` | 有 2 个以上互不依赖的任务时并行派发子代理 |
| `subagent-driven-development` | 在当前会话内用子代理执行计划中的独立任务 |
| `using-git-worktrees` | 需要隔离工作区时用 git worktree 开辟独立目录 |
| `finishing-a-development-branch` | 开发完成后引导选择 merge / PR / 清理分支 |
| `writing-skills` | 创建、编辑、验证新的 skill |

### understand-anything 明细

| Skill | 用途 |
| --- | --- |
| `understand` | 分析代码库生成可交互知识图谱（架构、组件、关系） |
| `understand-chat` | 基于知识图谱问答，理解代码库 |
| `understand-dashboard` | 启动 Web 仪表盘可视化代码库知识图谱 |
| `understand-diff` | 分析 git diff / PR：变更内容、影响面、风险 |
| `understand-domain` | 提取业务领域知识，生成交互式领域流程图 |
| `understand-explain` | 深度解读指定文件、函数或模块 |
| `understand-knowledge` | 分析 LLM wiki 知识库，生成实体/关系/主题知识图谱 |
| `understand-onboard` | 为新成员生成项目上手指南 |

## 单体 `standalone/`

### research/ 调研资讯

| Skill | 状态 | 用途 |
| --- | --- | --- |
| `last30days` | ✅ 在用 | 跨 Reddit/X/YouTube/TikTok/HN/Polymarket 调研任意主题近 30 天真实讨论与热度（v3.3.2，已剔除演示 assets） |
| `aihot` | ✅ 在用 | 拉取 AI HOT 公开 API，整理当日 AI 圈资讯中文简报 |

### frontend-design/ 前端设计

| Skill | 状态 | 用途 |
| --- | --- | --- |
| `impeccable` | ✅ 在用 | 前端界面设计/重设计/审查/打磨的综合 UX 方法论 |
| `taste-skill` | ✅ 在用 | 反模板化前端：落地页、作品集、重设计的"去 AI 味"设计 |
| `gpt-tasteskill` | ✅ 在用 | 高级 UX/UI + GSAP 滚动动效工程（AIDA 结构、bento 网格） |
| `soft-skill` | ✅ 在用 | 高端代理公司级设计规范：字体、间距、阴影、卡片、动画 |
| `redesign-skill` | ✅ 在用 | 升级现有网站/应用到高端质感，不破坏功能 |
| `uncodixfy` | ✅ 在用 | 生成前端代码时阻止典型 AI 味 UI，向 Linear/Stripe 风格看齐 |
| `minimalist-skill` | ✅ 在用 | 极简编辑风界面：暖色单色调、扁平 bento、无渐变 |
| `brutalist-skill` | ✅ 在用 | 粗野主义界面：瑞士排版 + 军用终端风，适合数据密集型页面 |
| `stitch-skill` | ✅ 在用 | 为 Google Stitch 生成语义化 DESIGN.md 设计系统文件 |
| `output-skill` | ✅ 在用 | 强制完整代码输出，禁占位符，处理 token 截断 |
| `image-to-code-skill` | ✅ 在用 | 先自己生成设计图、深度分析，再按图实现网站代码 |

### imagegen/ 图像生成

| Skill | 状态 | 用途 |
| --- | --- | --- |
| `imagegen-frontend-web` | ✅ 在用 | 为网站每个 section 生成一张高端横版设计参考图 |
| `imagegen-frontend-mobile` | ✅ 在用 | 生成 iOS/Android 移动端 App 界面概念图（带手机壳） |
| `brandkit` | ✅ 在用 | 生成高端品牌手册：logo 系统、识别规范、视觉世界观 |
| `hatch-pet` | ✅ 在用 | 创建/修复/打包 Codex 动画宠物精灵图（8x9 atlas + pet.json） |

### tools/ 实用工具

| Skill | 状态 | 用途 |
| --- | --- | --- |
| `pdf` | ✅ 在用 | 读取、创建、审查 PDF（reportlab / pdfplumber / pypdf + 渲染校验） |
| `playwright` | ✅ 在用 | 终端驱动真实浏览器：导航、填表、截图、抓数据、调试 UI 流程 |

### misc/ 其他

| Skill | 状态 | 用途 |
| --- | --- | --- |
| `meihua-yishu` | ✅ 在用 | 梅花易数占卜：起卦、解卦、测字 |

## 外部参考仓库（非本地 skill）

| 仓库 | 类型 | 用途 |
| --- | --- | --- |
| [DavidHDev/react-bits](https://github.com/DavidHDev/react-bits) | React 组件库 | 📖 已快照入 `reference/react-bits`（b8f0d67，剔除网站资源后 17MB）。前端实现素材，不是 skill |
| [mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill) | 单体 skill | 已于 2026-06-12 安装为本地 `last30days`（安全审查通过，见知识库登记页） |
| [mattpocock/skills](https://github.com/mattpocock/skills) | skill 集 | 📖 已快照入 `reference/mattpocock-skills`（694fa30）。按需挑选提为在用，提用前走安全审查 |
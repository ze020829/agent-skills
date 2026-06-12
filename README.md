# Agent Skills 总览

本目录存放所有自定义 / 第三方 Codex Agent Skills。每个子目录一个 skill，入口为 `SKILL.md`。
按需检索下表，找到对应功能后阅读该 skill 的 `SKILL.md` 使用。

> 注：`.system/` 为运行时目录，不属于 skill；`create-yourself/selves/` 含个人数据，不随仓库分发。

## 开发流程 / 工程方法（superpowers 系列）

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

## 前端设计 / UI 风格

| Skill | 用途 |
| --- | --- |
| `impeccable` | 前端界面设计/重设计/审查/打磨的综合 UX 方法论 |
| `taste-skill` | 反模板化前端：落地页、作品集、重设计的"去 AI 味"设计 |
| `taste-skill-v1` | taste-skill 的 v1 旧版，仅为兼容旧项目保留 |
| `gpt-tasteskill` | 高级 UX/UI + GSAP 滚动动效工程（AIDA 结构、bento 网格） |
| `soft-skill` | 高端代理公司级设计规范：字体、间距、阴影、卡片、动画 |
| `redesign-skill` | 升级现有网站/应用到高端质感，不破坏功能 |
| `uncodixfy` | 生成前端代码时阻止典型 AI 味 UI，向 Linear/Stripe 风格看齐 |
| `minimalist-skill` | 极简编辑风界面：暖色单色调、扁平 bento、无渐变 |
| `brutalist-skill` | 粗野主义界面：瑞士排版 + 军用终端风，适合数据密集型页面 |
| `stitch-skill` | 为 Google Stitch 生成语义化 DESIGN.md 设计系统文件 |
| `output-skill` | 强制完整代码输出，禁占位符，处理 token 截断 |

## 图像生成 / 视觉产出

| Skill | 用途 |
| --- | --- |
| `imagegen-frontend-web` | 为网站每个 section 生成一张高端横版设计参考图 |
| `imagegen-frontend-mobile` | 生成 iOS/Android 移动端 App 界面概念图（带手机壳） |
| `image-to-code-skill` | 先自己生成设计图、深度分析，再按图实现网站代码 |
| `brandkit` | 生成高端品牌手册：logo 系统、识别规范、视觉世界观 |
| `hatch-pet` | 创建/修复/打包 Codex 动画宠物精灵图（8x9 atlas + pet.json） |

## 项目理解 / 知识图谱（understand 系列）

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

## 实用工具

| Skill | 用途 |
| --- | --- |
| `pdf` | 读取、创建、审查 PDF（reportlab / pdfplumber / pypdf + 渲染校验） |
| `playwright` | 终端驱动真实浏览器：导航、填表、截图、抓数据、调试 UI 流程 |

## 资讯 / 其他

| Skill | 用途 |
| --- | --- |
| `aihot` | 拉取 AI HOT 公开 API，整理当日 AI 圈资讯中文简报 |
| `create-yourself` | 把聊天记录/日记/照片蒸馏成可运行的"数字自己" |
| `meihua-yishu` | 梅花易数占卜：起卦、解卦、测字 |

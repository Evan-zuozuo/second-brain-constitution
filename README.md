# second-brain-constitution · 宪法驱动的知识库治理体系

> 一套让个人 / 团队知识库**不失控**的治理方法论：先立宪法，再养知识。
> 不是又一个笔记模板合集，而是一套经过 **1497 篇笔记、9715 文件跨机迁移实战检验**的规则体系。

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

---

## 一、项目定位

大多数知识库死于同一条曲线：**前两周热情满满，第三周堆成垃圾场，第四周不敢打开。**

本项目给出解法：**用「宪法」治理知识库**——一套最高效力的规则文件 + 配套落位规则 + AI 协作边界 + 沉淀流水线 + 11 个开箱模板，让知识库从「收藏夹」变成「可复用、可检索、可回溯的资产」。

核心机制一览：

| 机制 | 一句话 |
|---|---|
| PARA + 卡片盒混合结构 | 领域（关注什么）与知识库（学到什么）分开，同一内容只放一处 |
| 命名前缀制 | `概念-` `排查-` `经验-` `SOP-` `项目-` `MOC-`……文件名唯一且可搜索 |
| 双链 + MOC 防孤岛 | 每条笔记至少 1 个出链/入链，新笔记必须挂到 MOC，孤岛率可控在 5% |
| frontmatter 八件套 | title/type/domain/status/created/updated/source/tags，`type` 反查落位 |
| 业务数据 A/B/C/D 分级 | A 直接入 / B 整理后入 / C 只入指针 / D 不入——按复用价值判，不按密级判 |
| AI 协作 L0–L3 自动化等级 | L0 只读 → L1 建议 → L2 自动落库 → L3 自动改（永不自动） |
| 永不删文件红线 | 只归档不删除，删除需经「待删除暂存区」由人最终处置 |

## 二、为什么需要「宪法」

没有宪法的知识库，有三种典型死法——本项目每一条规则都对准其中至少一种：

1. **孤岛死**：笔记之间没有链接，图谱上一堆游离点。写了 500 篇，能复用为 0。
   → 对策：双链强制 + MOC 兜底 + 每月孤岛巡检。
2. **台账化死**：把每天变的业务数字、大段原文、整篇转载往里倒，库成了化石仓库。
   → 对策：A/B/C/D 分级（不入当期值、只入结构和口径）+「不做素材仓库」边界 + 沉淀质量红线（一条笔记只讲一件事）。
3. **静默分叉死**：多台机器、多个 AI、多次迁移之后，同一个知识点出现两个版本，没人知道哪个是真的。
   → 对策：宪法最高效力 + 修改需明确授权 + 矛盾走 `[CONFLICT]` → 裁决 → `[RESOLVED]`，不静默改写 + 「被取代标注」模板（旧内容保留可回溯）。

**宪法的本质**：把「什么能进、放哪、怎么连、谁说了算」在**第一天**写死，防止第九百天的大返工。

## 三、快速开始（5 步搭起来）

```bash
# 0. 准备：安装 Obsidian，新建一个空 Vault 作为 <VAULT_ROOT>
```

1. **立宪法**：把 `docs/00-知识库宪法.md` 复制到 `<VAULT_ROOT>/00_系统/01_规则与公约/`，通读一遍，按需改边界条款。
2. **建骨架**：按宪法第二节创建 9 个顶层目录（`00_系统` ~ `08_归档`）。
3. **装模板**：把 `templates/` 整个目录复制到 `<VAULT_ROOT>/00_系统/02_模板/`，在 Obsidian 里用 Templater 指向该目录。
4. **接 AI**：把 `docs/03-AI协作规则.md` + `docs/06-操作说明书.md` 发给你的 AI 助手，让它进场必读；自动化等级默认 L1。
5. **跑通一次闭环**：往 `02_灵感文件/` 丢一条素材，对 AI 说「分析一下我的灵感文件」→ 看它产出沉淀提案 → 确认 → 落库 → 挂 MOC。跑通这一遍，体系就转起来了。

日常维护节奏（宪法第七节）：每次对话结束沉淀一次，每周清收件箱，每月查孤岛，每季度回顾领域。

## 四、目录结构

```
second-brain-constitution/
├── README.md                          # 本文件
├── LICENSE                            # CC-BY-4.0
├── docs/
│   ├── 00-知识库宪法.md                # 根本大法（最高效力，主材料）
│   ├── 01-分类落位速查表.md            # 拿到一条新信息，从上往下判断落点
│   ├── 02-归档与维护规则.md            # 只归档不删除 / 孤岛巡检 / 备份策略
│   ├── 03-AI协作规则.md                # 给 AI 的操作手册：边界 + 8 项硬校验
│   ├── 04-凭证管理规则.md              # 凭证能入/不能入的唯一落点与外传红线
│   ├── 05-快速开始.md                  # 插件安装 + 三个入门场景
│   ├── 06-操作说明书.md                # 库级 README：角色分工 / 目录速查 / 红线
│   └── case-study-migration.md         # 实战案例：三轮合并、1430 文件零缺失、93 个 PII 隔离
└── templates/
    ├── 概念笔记.md · 问题排查笔记.md · 经验教训.md · 流程SOP.md
    ├── 项目笔记.md · 日记.md · 灵感速记.md · 沉淀提案.md
    └── MOC索引.md · 体检报告.md · 被取代标注.md
```

## 五、实战案例（来自真实迁移）

`docs/case-study-migration.md` 记录了一次「先立宪法、再迁数据」的完整重建，关键数字：

- **三轮合并**完成跨机迁移：第 1 轮骨架 + 238 文件融入（BOM 清零、frontmatter 零缺失）；第 2 轮 1401 存量并入 + **1240 篇 frontmatter 宪法化**（零缺失）；第 3 轮旧结构归档 **1430 文件零缺失验证通过**。
- **93 个含 PII 文件实时检测隔离**（证件号/手机号/健康/财务/凭证），隔离区永不镜像。
- 迁移后活动区 **1497 篇**笔记、归档区 2078 篇，**孤儿笔记 74 篇（5%）**——由 MOC 机制兜底可控。
- 方法论沉淀：**集合一致性闸门**（比文件名集合而不是文件数，防静默内容丢失）。

## 六、适用场景

- **个人第二大脑**：一个人 + 一个 AI 助手，把工作知识和灵感沉淀成可复用资产。
- **团队知识库**：多人共写时，宪法 = 团队共识的显式化（命名、落位、边界），新人进场必读。
- **AI Agent 的记忆层**：给 Agent 一套「什么能记、记哪、怎么连、什么不能碰」的治理规则——L0–L3 自动化等级就是 Agent 的权限模型。
- **Obsidian / Logseq / 任意 md 双链库**：规则与工具解耦，结构可平移到任何双链笔记软件。

## 七、English Overview

**Second-Brain Constitution** is a governance methodology for personal/team knowledge bases: a supreme "constitution" file plus companion rules that keep a PKM vault from decaying into a junk drawer.

- **Structure**: PARA + Zettelkasten hybrid — `03_领域` (what you follow) vs `05_知识库` (what you learned); one note, one place, linked everywhere.
- **Naming**: prefix-based filenames (`概念-`, `排查-`, `经验-`, `SOP-`, `项目-`, `MOC-`…), unique and searchable.
- **Anti-orphan**: every note needs ≥1 link and must hang on a MOC (map of content); orphan rate kept ~5% in practice.
- **Metadata**: 8-field frontmatter; `type` determines folder location.
- **Business data grading A/B/C/D**: by reusability, not secrecy — A in, B structure-only with `snapshot_date`, C pointer-only, D never.
- **AI collaboration levels L0–L3**: read-only → propose → auto-write-new → auto-modify (never automatic).
- **Red lines**: never delete (archive only); never silently overwrite; conflicts resolved explicitly via `[CONFLICT]` → `[RESOLVED]`.
- **Battle-tested**: 1,497 active notes, 9,715-file cross-machine migration in three merge rounds, 1,430 files verified zero-loss, 93 PII files quarantined.

## 许可证

文档类资产，采用 [CC-BY-4.0](LICENSE)：自由使用、修改、商用，**保留署名**即可。

> 脱敏声明：本仓库所有规则、模板与案例均已脱敏（人名、公司名、路径、凭证、PII 均已移除或替换为占位符），可安全公开。

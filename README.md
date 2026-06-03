<div align="center">

# LLMInternSkill / LLM Intern Skill

**大模型实习简历与求职工具箱：LLM internship resume polish, JD tailoring, RAG / Agent / Post-training 项目包装、面试拷打、开源项目补强。**

<sub>一个面向大模型实习、AI 求职和 Codex Skill 工作流的 evidence-bound resume toolkit：不只是把简历写好听，而是让每一行都能扛住面试追问。</sub>

<sub>Keywords: LLM internship resume, 大模型实习简历, Codex Skill, resume polish, JD tailoring, interview prep, RAG, Agent, post-training, pretraining, search ranking, AIGC, multimodal.</sub>

<br>
<br>

![Type](https://img.shields.io/badge/type-Codex%20Skill-111827)
![License](https://img.shields.io/badge/license-MIT-blue)
![Focus](https://img.shields.io/badge/focus-LLM%20Internship-4f46e5)
![Method](https://img.shields.io/badge/method-evidence--bound-f59e0b)
![Language](https://img.shields.io/badge/language-ZH%20%2B%20EN-10b981)
![Status](https://img.shields.io/badge/status-final%20MVP-ec4899)
![GitHub Repo stars](https://img.shields.io/github/stars/couragec/llm-intern-skill?style=flat&label=stars)

[30 秒看懂](#30-秒看懂) · [快速开始](#快速开始) · [Seed 示例](#旗舰示例豆包-seed-搜索排序) · [功能地图](#功能地图) · [Star History](#star-history) · [参考](#参考)

</div>

---

## 30 秒看懂

| 你给它什么 | 它帮你做什么 |
| --- | --- |
| 一份原始简历 | 📝 润色成更清楚、更技术、更像实习候选人的表达 |
| 一个目标 JD | 🎯 判断匹配度，重排经历，生成定制版简历 |
| 一个材料文件夹 | 🔍 审计代码、项目素材、论文笔记、日志、截图和奖项 |
| 一堆单薄项目 | 🧪 包装成真实、可讲、能补证据的项目故事 |
| 一份担心被问穿的简历 | 🎤 生成面试官式追问、危险回答、及格回答、强回答 |
| 证据不足 | 🌱 推荐开源项目学习、复现、改造，形成新证据 |
| 最终要投递 | 📄 用 Bill Ryan LaTeX 模板生成 PDF-ready 简历草稿 |

核心判断：

```text
可以写 / 谨慎写 / 补证据后写 / 不能写 / 无法判断
```

核心产出：

```text
raw resume + materials/ + target_jd.txt
-> 简历润色
-> JD 匹配
-> 真实性边界
-> Evidence Contract
-> 定制简历
-> 面试拷打
-> 回答卡
-> 补证据计划
-> Project Scout
-> LaTeX 简历草稿
```

---

## 一眼 Before / After

<table>
  <tr>
    <th width="28%">原始简历</th>
    <th width="36%">安全润色版</th>
    <th width="36%">为什么这样写</th>
  </tr>
  <tr>
    <td>熟悉大模型与 RAG，优化搜索效果。</td>
    <td>围绕搜索相关性场景整理 query-doc 样例与长尾查询 bad case，分析歧义查询、时效性不足和低权威 DOC 对检索结果的影响。</td>
    <td>没有指标时不写“优化效果”；先把真实证据写成问题分析能力。</td>
  </tr>
  <tr>
    <td>完成企业级知识库问答系统。</td>
    <td>完成企业文档问答 demo 的文档切分、向量检索和 Prompt 模板配置，记录召回错误、引用错位和无依据回答等问题。</td>
    <td>没有上线、权限、监控和用户记录时，不写“企业级系统”。</td>
  </tr>
  <tr>
    <td>训练大模型并提升生成质量。</td>
    <td>复现小参数 LLM 的训练与推理流程，记录配置、日志、样例输出和 bad case，形成端到端理解笔记。</td>
    <td>没有数据、配置、训练日志和 checkpoint 时，不写“训练大模型”。</td>
  </tr>
</table>

一句话原则：

```text
润色可以让真实经历更清楚、更有技术含量；
但不能把没有证据的经历润色成事实。
```

---

## 快速开始

### 方式一：只想润色简历

```text
使用 LLMInternSkill。
请帮我做简历润色，但不要编造经历。

目标岗位：
[贴 JD 或写岗位方向]

我的原始简历：
[贴简历内容]

请输出：
1. Before / After
2. 哪些行可以写、哪些需要降级
3. 技术表达增强版
4. JD 定制版
5. 面试可能追问的问题
```

### 方式二：完整材料文件夹

准备：

```text
materials/
├── target_jd.txt
├── resume.md
├── projects/
├── code/
├── notes/
├── papers/
├── awards/
└── other/
```

然后说：

```text
Use LLMInternSkill on ./materials.
Generate resume polish, JD fit verdict, targeted resume, interview grilling,
answer cards, evidence upgrade plan, and project scout recommendations.
```

### 方式三：安装成 Codex Skill

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/couragec/llm-intern-skill.git ~/.codex/skills/llm-intern-skill
```

重启 Codex 或开启新会话后，直接说：

```text
使用 LLMInternSkill，读取我的 materials/ 文件夹。
```

---

## 旗舰示例：豆包 Seed 搜索排序

这个示例故意选了一个强 JD：豆包大模型团队 Seed 搜索 / Ranking / DOC 理解研究实习。

它展示了这个项目最核心的能力：

```text
强 JD + 弱/中等材料
-> 不硬吹 strong fit
-> 找到可写证据
-> 降级危险表达
-> 生成能投递的保守简历
-> 生成面试官会追问的问题
-> 给出 1 天 / 3 天 / 1 周补证据计划
```

直接看三份文件：

- [目标 JD](examples/doubao-seed-search-ranking-jd.md)
- [候选人材料输入](examples/doubao-seed-materials-input.md)
- [最终输出包](examples/doubao-seed-final-pack.md)
- [模拟 LaTeX 简历 PDF](examples/seed-resume-latex/seed-topseed-resume.pdf)

关键输出片段：

```text
Verdict: risky fit
Why: 有 RAG 和小搜索 demo，但缺 ranking metrics、强算法实习证据和 DOC 理解实验。
Fastest upgrade: 把 mini search demo 补成 BM25 vs embedding vs rerank 对比，加入 NDCG@10 / MRR 和 bad-case 分析。
```

---

## 功能地图

| Icon | 模块 | 输出 |
| --- | --- | --- |
| 📝 | Resume Polish | Before/After、技术表达增强、CN/EN 版本、ATS 关键词 |
| 🎯 | JD Tailoring | JD match table、定制版简历、岗位关键词重排 |
| 🔍 | Resume Diagnosis | 弱表达、风险 claim、缺证据、被问穿点 |
| 🧪 | Project Packaging | 项目 bullet、架构叙事、2-3 分钟项目故事 |
| 🛡 | Evidence Guard | Truth Boundary、Evidence Contract、危险表达降级 |
| 🎤 | Interview Drill | 逐行拷打、追问链、危险/及格/强回答 |
| 🌱 | Project Scout | 开源项目推荐、最小运行路径、改造点、可写证据 |
| 📄 | LaTeX Export | Bill Ryan 中文 LaTeX 模板、PDF-ready 简历草稿 |

---

## 输出长什么样

完整模式会生成：

```text
output/
├── 01_jd_analysis.md
├── 02_materials_audit.md
├── 03_truth_boundary.md
├── 04_evidence_contract.md
├── 05_resume_polish.md
├── 06_targeted_resume.md
├── 07_interview_grilling.md
├── 08_answer_cards.md
├── 09_upgrade_plan.md
├── 10_project_scout.md
└── 11_final_pack.md
```

简历润色模式会优先输出：

```text
1. Resume Polish Verdict
2. Before / After
3. Line-by-line diagnosis
4. Final polished resume section
5. Optional English version
6. Evidence upgrade list
```

---

## 支持岗位

| 方向 | 会重点检查什么 |
| --- | --- |
| RAG / 知识库问答 | chunk、retrieval、rerank、citation、eval、拒答、权限 |
| Agent / Tool Use | tool schema、参数校验、trace、重试、状态、人审 |
| Agentic RL | trajectory、environment、reward/verifier、GRPO/PPO、任务成功率 |
| Post-training / Alignment | SFT、DPO、RLHF/RLAIF、reward model、偏好数据、评估 |
| Pretraining / Mid-training | 数据引擎、tokenizer、训练配置、loss、分布式、污染检查 |
| LLM 应用工程 | structured output、prompt 版本、bad case、成本、延迟 |
| LLM 算法 | Transformer、SFT/LoRA/DPO、训练配置、日志、评测 |
| 搜索 / 推荐 / 排序 | query-doc、召回、粗排、rerank、NDCG/MRR、DOC 质量 |
| AIGC | 生成链路、质量评估、安全、人工复核、成本 |
| 多模态 | OCR/layout、VLM、跨模态检索、视觉 bad case |
| AI 后端 | API、队列、重试、观测、权限、部署、成本 |

---

## 为什么不只是简历润色器

普通简历润色器经常只做这件事：

```text
把一句普通话改成一句漂亮话。
```

LLMInternSkill 要多走三步：

```text
这句话有没有证据？
这句话会被面试官怎么追？
如果现在不能写，补什么证据后能写？
```

所以它不会把：

```text
做过 RAG demo
```

硬包装成：

```text
主导企业级智能知识库系统上线，显著提升业务效率。
```

它会更倾向于输出：

```text
完成企业文档问答 demo 的文档切分、向量检索和 Prompt 模板配置，
记录召回错误、引用错位和无依据回答等问题，
为后续 query-answer-evidence 评估集建设沉淀样例。
```

这就是它的差异化：**好听，但不虚。**

---

## Project Scout

当当前材料太弱时，LLMInternSkill 会建议你补项目，而不是硬写。

示例：

- MiniMind-style from-scratch LLM 项目
- RAG evaluation / citation accuracy 项目
- Search / rerank baseline 项目
- Agent tool-calling workflow 项目
- LLM inference / serving / quantization 项目

每个推荐都必须包含：

```text
why this fits
why not / risk
minimum run path
what to modify
what evidence to collect
resume-safe claim after completion
interview grilling questions
```

边界：

```text
学习开源项目不能直接包装成工作经历。
只有真实复现、理解、改造、记录证据后，才能写成个人项目或开源实践。
```

示例：[MiniMind Project Scout](examples/project-scout-minimind.md)

更多例子：

- [Resume Polish Before / After](examples/resume-polish-before-after.md)
- [Prompt-only Work Safely Downgraded](examples/prompt-only-downgrade.md)
- [Search / Rerank Project Scout](examples/project-scout-search-rerank.md)
- [LoRA Experiment With Weak Metrics](examples/lora-weak-metrics.md)
- [Post-training / Agentic RL Case](examples/posttraining-agentic-rl-case.md)
- [Seed Resume LaTeX Demo](examples/seed-resume-latex/README.md)

---

## LaTeX 简历模板

默认使用 Bill Ryan's elegant LaTeX resume 的中文模板：

```text
templates/resume-latex/bill-ryan-elegant-zh_CN/
```

来源：

- Overleaf: <https://www.overleaf.com/latex/templates/bill-ryans-elegant-latex-resume/xcqmhktmzmsw>
- Upstream: <https://github.com/billryan/resume>

说明：

- 中文入口：`resume-zh_CN.tex`
- 编译方式：XeLaTeX
- 保留 upstream attribution 和 license
- 大号 CJK 字体本地保留但不进 Git

---

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=couragec/llm-intern-skill&type=Date)](https://www.star-history.com/#couragec/llm-intern-skill&Date)

---

## 参考

本项目参考和学习了以下开源项目，感谢这些项目的启发：

- [`resumify`](https://github.com/breaker505/resumify)
- [`shushu-internship-resume-optimizer`](https://github.com/Sunanzhe2004/shushu-internship-resume-optimizer)
- [`shushu-internship-tool`](https://github.com/LiuMengxuan04/shushu-internship-tool)
- [`shushu-ProjectProof`](https://github.com/YingaoWang-casia/shushu-ProjectProof)
- [`vibe-resume`](https://github.com/LiuMengxuan04/vibe-resume)
- [`resuml`](https://github.com/phoinixi/resuml)
- [`Auto-claude-code-research-in-sleep`](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep)

---

## 仓库结构

```text
.
├── SKILL.md
├── skill-references/
│   ├── resume-polish.md
│   ├── resume-tailoring.md
│   └── roles/
├── templates/
│   ├── resume-polish-report.md
│   └── resume-latex/
├── examples/
├── evals/
├── docs/
└── agents/
```

欢迎通过 issue / PR 补充更多 JD、案例、角色参考和 eval。

## License

MIT. The bundled Bill Ryan resume template keeps its upstream license and attribution; see `templates/resume-latex/README.md`.

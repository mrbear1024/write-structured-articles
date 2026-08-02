# 结构化文章写作 Skill

一个面向 Codex 的中文写作技能，把主题、素材、采访、研究笔记或现有草稿组织成判断清晰、论证完整、边界明确且可行动的文章。

它不是固定格式的文章模板，而是一条可复用的推理路径：

```text
具体变化或问题
    -> 必要背景
    -> 核心判断
    -> 事实与因果论证
    -> 适用边界
    -> 可执行收获
    -> 结尾承诺
```

## 能做什么

- 从主题和素材生成文章大纲或完整初稿
- 在保留作者事实、观点和声音的前提下重写草稿
- 评审文章的结构、证据、因果、边界和行动建议
- 区分事实、他人观点、作者判断、推断与不确定性
- 把七部分变成自然的文章结构，而不是机械填空

## 安装

克隆仓库：

```bash
git clone https://github.com/mrbear1024/write-structured-articles.git
```

复制技能目录到 Codex 的技能目录：

```bash
mkdir -p ~/.codex/skills
cp -R write-structured-articles/skills/write-structured-articles ~/.codex/skills/
```

安装后，在新的 Codex 任务中即可显式调用：

```text
使用 $write-structured-articles，根据这份研究笔记写一篇面向产品经理的文章。
```

也可以直接提出这类需求，由 Codex 根据技能描述自动匹配：

```text
请评审这篇草稿，重点检查核心判断、因果链和适用边界，不要重写全文。
```

## 仓库结构

```text
skills/write-structured-articles/
├── SKILL.md
└── agents/
    └── openai.yaml
```

- `SKILL.md`：触发条件、写作流程和交付前检查
- `agents/openai.yaml`：Codex 界面中的名称、简介和默认提示词

## 设计原则

1. 先确定文章要解决的具体问题和核心判断。
2. 用事实、案例和因果解释支撑判断，不堆砌材料。
3. 主动说明成立条件、反例和未知。
4. 给读者一个可以复用的框架、决策问题或下一步动作。
5. 保留作者声音，不虚构数据、案例、引语或来源。

## 贡献

欢迎提交 Issue 或 Pull Request。修改技能后，请确保 `SKILL.md` 的 YAML frontmatter 只包含 `name` 和 `description`，并使用 Codex 的 `quick_validate.py` 校验技能目录。

## 许可证

[MIT](LICENSE)

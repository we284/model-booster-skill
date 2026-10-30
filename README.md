# model-booster-skill

Claude Opus 5.5 的 `model-booster` skill（v1.2.3）。

本仓库用于存放并分享该 skill，包含 `SKILL.md`、`memory.md` 及 `references/` 下的参考工作流文档。核心能力：对抗式自我批判、事实台账、写作 / 代码 / 推理 / 决策复盘 / 研究 等工作流。

## 目录结构

```
model-booster-skill/
├── SKILL.md                        # skill 入口与说明
├── memory.md                       # 记忆 / 上下文文件
└── references/                     # 各类工作流与评测参考
    ├── aux-rules.md                # 辅助规则
    ├── code-workflow.md            # 代码工作流
    ├── critique-rubrics.md         # 批判量表
    ├── decision-review-workflow.md # 决策复盘工作流
    ├── identity-opus55.md          # 身份设定（Claude Opus 5.5）
    ├── reasoning-workflow.md       # 推理工作流
    ├── research-workflow.md        # 研究工作流
    └── writing-workflow.md         # 写作工作流
```

## 安装 / 使用

skill 载体是一个名为 `model-booster` 的文件夹（内含 `SKILL.md`）。把它放进你所用工具的 **skills 目录** 即可启用。

### Claude Code

```bash
# 克隆本仓库
git clone https://github.com/we284/model-booster-skill.git

# 把仓库内容作为 skill 放入用户级 skills 目录（文件夹名为 model-booster）
mkdir -p ~/.claude/skills/model-booster
cp -r model-booster-skill/. ~/.claude/skills/model-booster/

# 或放入项目级目录（在项目根目录）
mkdir -p .claude/skills/model-booster
cp -r model-booster-skill/. .claude/skills/model-booster/
```

重启 / 重新加载会话后，skill 即可被识别调用。

### CodeBuddy / 其他支持 skills 的工具

原理相同：将本仓库内容放入对应工具的 skills 目录（文件夹名保持 `model-booster`），具体路径请参照该工具的 skills 文档。

## 说明

- 仓库内容即 skill 本体，无需额外构建步骤。
- 如上游发布新版本，本仓库会同步更新 `main` 分支。

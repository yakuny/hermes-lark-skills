# Hermes Lark Skills

> Hermes Agent 飞书 lark-cli 技能包 — 24 个 Lark API Skills，开箱即用

## 📦 包含的 Skills

| Skill | 功能 |
|-------|------|
| `lark-approval` | 审批流程 |
| `lark-attendance` | 考勤打卡 |
| `lark-base` | 多维表格 |
| `lark-calendar` | 日历日程 |
| `lark-contact` | 通讯录 |
| `lark-doc` | 飞书文档 |
| `lark-drive` | 云空间 |
| `lark-event` | 事件订阅 |
| `lark-im` | 消息 |
| `lark-mail` | 飞书邮箱 |
| `lark-markdown` | Markdown |
| `lark-minutes` | 妙记 |
| `lark-okr` | OKR |
| `lark-openapi-explorer` | OpenAPI 探索 |
| `lark-shared` | 共享工具 |
| `lark-sheets` | 电子表格 |
| `lark-skill-maker` | Skill 制作器 |
| `lark-slides` | 幻灯片 |
| `lark-task` | 任务 |
| `lark-vc` | 视频会议 |
| `lark-whiteboard` | 白板 |
| `lark-wiki` | 知识库 |
| `lark-workflow-meeting-summary` | 会议纪要工作流 |
| `lark-workflow-standup-report` | 站会报告工作流 |

## 🚀 快速开始

### 1. 安装 lark-cli

```bash
npm install -g lark-cli
```

### 2. 配置密钥

```bash
# 复制配置模板
cp config.example.json ~/.lark-cli/hermes/config.json

# 编辑填入你自己的 appId 和 appSecret
# 在飞书开放平台创建应用获取: https://open.feishu.cn
```

### 3. 安装 Skills

将本仓库中的 `lark-*` 目录复制到 Hermes 的 skills 目录：

```bash
cp -r lark-* ~/.agents/skills/
```

或使用符号链接（推荐，方便同步更新）：

```bash
for skill in lark-*; do
  ln -sf "$(pwd)/$skill" ~/.agents/skills/$skill
done
```

### 4. 设置环境变量

在 `~/.hermes/.env` 中添加：

```
LARK_APP_ID=cli_xxxxxxxxxx
LARK_APP_SECRET=your_secret_here
```

## 🔒 安全说明

- ⚠️ **永远不要** 将真实的 `appSecret` 提交到 Git 仓库
- 使用 `config.example.json` 作为模板，实际配置文件已加入 `.gitignore`
- 每个使用者需要自己在[飞书开放平台](https://open.feishu.cn)创建应用

## 📝 更新

```bash
cd ~/.agents/skills
git pull origin main
```

## 📄 License

MIT

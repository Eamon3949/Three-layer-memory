# Three-Layer Memory System for OpenClaw

永不失忆的 AI Agent 记忆系统。

## 快速开始

1. 创建 memory 目录：
```bash
mkdir memory
```

2. 添加 cron jobs：
```bash
openclaw cron add < cron-daily.json
openclaw cron add < cron-weekly.json
openclaw cron add < cron-hourly.json
```

3. 初始化索引：
```bash
openclaw memory index
```

4. 更新 AGENTS.md，添加记忆检索规则（见 SKILL.md）

## 架构

- **Daily Sync** (21:00) - 捕获当天对话
- **Weekly Compound** (周日 22:00) - 蒸馏精华
- **Hourly Micro-Sync** (每2小时) - 安全网
- **Semantic Search** - 语义检索

## 使用

```bash
openclaw memory search "查询内容"
```

详见 SKILL.md

# Genius Three-Layer Memory System

天才级永不失忆的 AI Agent 记忆系统。

## 特性

- 🧠 主动反思与矛盾检测
- 🔗 因果链提取
- 💡 模式发现（8-15条洞见）
- 📊 重要性评分（0-100）
- 🗺️ 知识图谱维护
- ⚡ 主动唤醒机制

## 快速开始

1. 创建文件结构：
```bash
mkdir memory
touch INSIGHTS.md RELATIONSHIPS.md
```

2. 添加 cron jobs：
```bash
openclaw cron add < cron-daily.json
openclaw cron add < cron-weekly.json
openclaw cron add < cron-hourly.json
```

3. 更新 AGENTS.md（添加主动唤醒规则）

4. 初始化索引：
```bash
openclaw memory index
```

## 架构

- **Hourly Micro-Sync** (每2小时) - 评分 >70 才写入
- **Daily Sync** (21:00) - 捕获当天对话
- **Weekly Genius Compound** (周日 22:00) - 8步超级蒸馏
- **Proactive Recall** - 每次回答前自动搜索

## 使用

```bash
openclaw memory search "查询内容"
```

详见 SKILL.md

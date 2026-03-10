# Genius Three-Layer Memory System

天才级永不失忆的 AI Agent 记忆系统。

## 核心能力

- 主动反思与矛盾检测
- 因果链提取（5-10条）
- 模式发现（8-15条洞见）
- 重要性评分（0-100分）
- 知识图谱维护
- 主动唤醒相关记忆

## 三层架构

1. **Hourly Micro-Sync** (每2小时) - 评分 >70 才写入
2. **Daily Memory Sync** (21:00) - 捕获当天对话
3. **Weekly Genius Compound** (周日 22:00) - 8步超级蒸馏

## 文件结构

```
workspace/
├── MEMORY.md              # 长期精华
├── INSIGHTS.md            # 每周洞见
├── RELATIONSHIPS.md       # 知识图谱
└── memory/
    └── YYYY-MM-DD.md     # 每日日志
```

## 快速开始

1. 创建文件：
```bash
mkdir memory
touch INSIGHTS.md RELATIONSHIPS.md
```

2. 添加 cron jobs（见 cron-*.json）

3. 更新 AGENTS.md 添加主动唤醒规则

4. 初始化索引：
```bash
openclaw memory index
```

详见各配置文件。

# Three-Layer Memory System

## 描述
永不失忆的 AI Agent 记忆系统。通过三层自动化架构（Daily/Weekly/Hourly + 语义搜索）实现持续记忆积累。

## 核心架构

### Layer 1: Daily Memory Sync
每晚 21:00 自动捕获当天所有对话，蒸馏成结构化日志

### Layer 2: Weekly Memory Compound  
每周日 22:00 提取一周精华，更新 MEMORY.md

### Layer 3: Hourly Micro-Sync
每2小时检查（9-23点），防止重要信息遗漏

### Layer 4: Semantic Search
使用 `openclaw memory search` 进行语义检索

## 文件结构

```
workspace/
├── MEMORY.md              # 精华记忆，每次 session 自动注入
├── memory/
│   ├── 2026-03-10.md     # 每日日志
│   ├── 2026-03-11.md
│   └── ...
```

## 安装步骤

### 1. 创建 memory 目录
```bash
mkdir memory
```

### 2. 配置三个 Cron Jobs

使用 `openclaw cron add` 或通过 cron tool 添加以下配置。

#### Job 1: Daily Memory Sync
- 时间：每晚 21:00
- 模型：Sonnet (省钱)
- 任务：捕获当天对话，写入日志

#### Job 2: Weekly Memory Compound
- 时间：每周日 22:00
- 模型：Sonnet
- 任务：蒸馏一周精华到 MEMORY.md

#### Job 3: Hourly Micro-Sync
- 时间：每2小时（9/11/13/15/17/19/21/23点）
- 模型：Sonnet
- 任务：检查最近活动，有则追加

### 3. 初始化搜索索引
```bash
openclaw memory index
```

### 4. 更新 AGENTS.md
添加记忆检索规则和立即写入机制。

## 使用方法

### 搜索记忆
```bash
openclaw memory search "上周关于项目的讨论"
```

### 手动索引
```bash
openclaw memory index
```

### 查看状态
```bash
openclaw memory status
```

## 核心原则

1. **分层存储** - 不把所有东西塞进 context window
2. **自动化** - 不依赖人工维护
3. **语义搜索** - 按需检索，不暴力读取
4. **立即写入** - 重要事件不等定时任务

## 效果

- ✅ 零失忆
- ✅ 记忆会复利增长
- ✅ 搜索速度快
- ✅ Token 消耗低

## 致谢

灵感来源：[@ericosiu](https://x.com/ericosiu) 的 agent memory infrastructure 文章

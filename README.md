# Let's Go Skills

OpenClaw 技能集合 - 让 AI 助手更强大的工具包

---

## 📦 技能列表

| 技能名称 | 版本 | 描述 |
|---------|------|------|
| [travel-planner](./travel-planner) | v1.0.0 | 智能旅行攻略生成器 - 支持多格式输入，联网查询景点天气，输出完整 Markdown 攻略 |

---

## 🚀 快速开始

### 安装技能

```bash
# 1. 克隆仓库
git clone https://github.com/revenger29624/lets-go-skills.git

# 2. 复制技能到 OpenClaw 目录
# Windows:
copy lets-go-skills\travel-planner\SKILL.md %USERPROFILE%\.qclaw\skills\travel-planner\
xcopy /E /I lets-go-skills\travel-planner\* %USERPROFILE%\.qclaw\skills\travel-planner\

# Mac/Linux:
cp -r lets-go-skills/travel-planner ~/.qclaw/skills/

# 3. 重启 OpenClaw
openclaw gateway restart
```

### 或者直接下载打包文件

```bash
# Windows PowerShell
Invoke-WebRequest -Uri "https://github.com/revenger29624/lets-go-skills/releases/download/v1.0.0/travel-planner.skill" -OutFile "$env:USERPROFILE\.qclaw\skills\travel-planner.skill"

# 解压后重启 OpenClaw
```

---

## 🧳 Travel Planner 使用示例

### 文字输入
```
帮我做一个去成都5天4晚的旅行攻略，想看大熊猫和吃美食
```

### 文件输入
```
请根据这个文件帮我规划旅行：[上传 travel-plan.txt]
```

### 输出示例
生成完整的 Markdown 攻略，包含：
- 📍 每日详细行程
- 🍜 美食推荐
- 🚗 交通指南
- 💰 费用预算
- 📝 必备清单

---

## 📁 仓库结构

```
lets-go-skills/
├── travel-planner/              # 技能源代码
│   ├── SKILL.md                 # 核心技能文档
│   ├── scripts/
│   │   └── parse_travel_input.py    # 输入文件解析器
│   ├── references/
│   │   └── destination_checklist.md # 目的地参考数据
│   └── assets/                  # 模板资源（可选）
├── travel-planner.skill         # 打包好的技能文件
└── README.md                    # 本文件
```

---

## 🛠️ 开发技能

### 创建新技能

参考 [OpenClaw Skill Creator](https://github.com/openclaw/skill-creator) 文档

```bash
# 初始化新技能
python scripts/init_skill.py my-skill --path ~/.qclaw/skills

# 打包技能
python scripts/package_skill.py my-skill
```

### 技能规范

- **SKILL.md** 必须包含 YAML frontmatter（name + description）
- **description** 要详细说明触发条件和功能
- **scripts/** 存放可执行代码
- **references/** 存放参考资料
- **assets/** 存放模板资源

---

## 📄 许可证

[MIT](./LICENSE) © 2024 revenger29624

---

## 🤝 贡献

欢迎提交 PR 和 Issue！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/amazing-skill`)
3. 提交更改 (`git commit -m 'Add amazing skill'`)
4. 推送分支 (`git push origin feature/amazing-skill`)
5. 创建 Pull Request

---

## 📮 联系方式

- GitHub: [@revenger29624](https://github.com/revenger29624)
- Issues: [提交问题](https://github.com/revenger29624/lets-go-skills/issues)

# 阿里巴巴Java开发手册 Skills

本项目将《阿里巴巴Java开发手册(黄山版)》PDF文档转换为通用的AI Agent Skills，支持多种AI/IDE平台(Claude、Codex、Cursor等)
，方便在开发过程中快速查阅和应用Java开发规约。

## 📚 项目简介

本项目的Skills基于阿里巴巴集团技术团队编写的《Java开发手册（黄山版）》，该手册是Java社区集体智慧结晶和经验总结，经历了多次大规模一线实战的检验及不断完善。手册以Java开发者为中心视角，划分为七个维度，再根据内容特征细分成若干二级子目录。

## 🎯 手册愿景

**码出高效，码出质量**

现代软件架构的复杂性需要协同开发完成，适当的规范和标准绝不是消灭代码内容的创造性、优雅性，而是限制过度个性化，以一种普遍认可的统一方式一起做事，提升协作效率，降低沟通成本。

## 🎯 跨平台适配

本项目的Skills采用**统一的SKILL.md格式标准**,支持多种AI/IDE平台(Claude、Codex、Cursor等)。

## 📁 Skills目录结构

```
skills/
├── java-coding-standards/        # 编程规约(通用)
│   └── SKILL.md
├── java-exception-logging/       # 异常日志(通用)
│   └── SKILL.md
├── java-unit-testing/            # 单元测试(通用)
│   └── SKILL.md
├── java-security-standards/      # 安全规约(通用)
│   └── SKILL.md
├── java-mysql-database/          # MySQL数据库(通用)
│   └── SKILL.md
├── java-project-structure/       # 工程结构(通用)
│   └── SKILL.md
├── java-design-standards/        # 设计规约(通用)
│   └── SKILL.md
├── README.md                     # 英文说明文档
└── README.zh.md                  # 中文说明文档
```

**说明:** 所有skills均已重构为**通用格式**,删除了平台特定的副本(.claude/、.codex/、.cursor/),统一使用单一SKILL.md文件。

## 🚀 如何使用

### 安装Skills

使用以下命令安装所需的Skill：

```bash
# 查看所有可用的Skills
npx skills add https://github.com/millet0328/Alibaba-Java-Coding-Guidelines --list

# 安装单个Skill
npx skills add https://github.com/millet0328/Alibaba-Java-Coding-Guidelines --skill java-coding-standards

# 安装多个指定的Skills
npx skills add https://github.com/millet0328/Alibaba-Java-Coding-Guidelines --skill java-coding-standards java-exception-logging java-mysql-database

# 一次性安装所有Skills(推荐)
npx skills add https://github.com/millet0328/Alibaba-Java-Coding-Guidelines
```

### 跨平台使用

这些Skills采用统一格式,可被多种AI/IDE平台自动识别和加载:

- **Claude** - Claude Desktop / Claude.ai
- **Codex** - OpenAI Codex
- **Cursor** - Cursor IDE
- 以及其他支持SKILL.md格式的AI Agent平台

### 自动触发

当你在编写Java代码时,AI会根据上下文自动激活相关的Skill,为你提供规约建议。

### 手动触发

你也可以通过以下方式使用：

1. **代码审查时** - 询问AI助手："请根据阿里巴巴Java开发手册检查这段代码"
2. **编写代码时** - 询问AI助手："如何按照阿里巴巴规约命名这个类？"
3. **设计数据库时** - 询问AI助手："根据MySQL规约，这个表设计合理吗？"

### 示例对话

```
用户: 如何命名一个用户服务类？
AI助手: 根据阿里巴巴Java开发手册编程规约，类名使用UpperCamelCase风格...
```

```
用户: 这段异常处理代码符合规范吗？
AI助手: 根据异常日志规约，建议使用...
```

## 📖 Skills列表

### 1. java-coding-standards（编程规约）

**描述：** 阿里巴巴Java开发手册编程规约，包含命名风格、常量定义、代码格式、OOP规约、日期时间、集合处理、并发处理、控制语句、注释规约等。

**使用场景：**

- 编写Java代码时
- 代码审查时
- 遵循阿里巴巴Java编码标准时

**主要内容：**

- (一) 命名风格 - 类名、方法名、变量名等命名规范
- (二) 常量定义 - 常量定义和使用规范
- (三) 代码格式 - 代码格式、缩进、换行等规范
- (四) OOP规约 - 面向对象编程规范
- (五) 日期时间 - 日期时间处理规范
- (六) 集合处理 - 集合类使用规范
- (七) 并发处理 - 多线程和并发编程规范
- (八) 控制语句 - if/for/while等控制语句规范
- (九) 注释规约 - 代码注释规范
- (十) 前后端规约 - 前后端交互规范
- (十一) 其他 - 其他编程规约

### 2. java-exception-logging（异常日志）

**描述：** 阿里巴巴Java开发手册异常日志规约，包含错误码、异常处理、日志规约。

**使用场景：**

- 处理异常时
- 编写日志代码时
- 设计错误码体系时

**主要内容：**

- (一) 错误码 - 错误码设计原则和规范
- (二) 异常处理 - 异常捕获和处理规范
- (三) 日志规约 - 日志记录和输出规范

### 3. java-unit-testing（单元测试）

**描述：** 阿里巴巴Java开发手册单元测试规约。

**使用场景：**

- 编写单元测试时
- 编写测试用例时
- 测试Java代码时

**主要内容：**

- AIR原则（自动化、独立性、可重复）
- 单元测试编写规范
- 测试用例设计规范
- Mock和Stub使用规范

### 4. java-security-standards（安全规约）

**描述：** 阿里巴巴Java开发手册安全规约。

**使用场景：**

- 实现安全功能时
- 处理认证授权时
- 应用安全最佳实践时

**主要内容：**

- 权限控制校验
- 敏感数据脱敏
- SQL注入防护
- XSS防护
- 参数验证
- 其他安全规范

### 5. java-mysql-database（MySQL数据库）

**描述：** 阿里巴巴Java开发手册MySQL数据库规约，包含建表规约、索引规约、SQL语句、ORM映射。

**使用场景：**

- 设计数据库架构时
- 编写SQL查询时
- 使用MySQL时

**主要内容：**

- (一) 建表规约 - 数据库表设计规范
- (二) 索引规约 - 索引设计和优化规范
- (三) SQL语句 - SQL编写规范
- (四) ORM映射 - ORM框架使用规范

### 6. java-project-structure（工程结构）

**描述：** 阿里巴巴Java开发手册工程结构规约，包含应用分层、二方库依赖、服务器。

**使用场景：**

- 构建Java项目结构时
- 管理依赖时
- 组织项目架构时

**主要内容：**

- (一) 应用分层 - 应用分层架构规范
- (二) 二方库依赖 - 依赖管理规范
- (三) 服务器 - 服务器配置规范

### 7. java-design-standards（设计规约）

**描述：** 阿里巴巴Java开发手册设计规约。

**使用场景：**

- 设计软件架构时
- 应用设计模式时
- 做设计决策时

**主要内容：**

- 存储方案和数据结构设计
- 需求分析（用例图、状态图、时序图、类图、活动图）
- 系统依赖设计
- 其他设计规范

## 🔍 规约分类

手册中的规约依据约束力强弱及故障敏感性，依次分为三大类：

- **【强制】** - 必须严格遵守，违反可能导致严重问题
- **【推荐】** - 建议遵循，有助于提升代码质量
- **参考** - 参考性建议，可根据实际情况选择

## 📝 规约说明格式

每个规约条目包含以下信息：

- **说明** - 对规约的适当扩展和解释
- **正例** - 提倡的编码和实现方式
- **反例** - 需要提防的雷区，以及真实的错误案例

## 📊 统计信息

- **总Skills数量:** 7个(通用格式)
- **SKILL.md格式:** 统一标准,跨平台兼容
- **原PDF页数:** 55页
- **版本:** 黄山版(1.7.1)
- **手册原始发布日期:** 2022年2月3日
- **Skills重构日期:** 2024年5月25日(合并为通用格式)

## 📄 内容来源

- **原始文档：** 《阿里巴巴Java开发手册（黄山版）》
- **制定团队：** 阿里巴巴集团技术团队
- **版本历史：** 黄山版新增11条新规约

## 🔗 相关资源

- [阿里巴巴Java开发手册官网](https://developer.aliyun.com/special/tech-java)
- [Java开发规约IDE插件](https://github.com/alibaba/p3c)
- [配套详解图书《码出高效》](https://developer.aliyun.com/special/tech-java)

## 📌 注意事项

1. **通用格式** - 所有skills已重构为统一格式,适配所有AI/IDE平台
2. 这些Skills是基于PDF文档转换生成的,内容保持原样
3. 建议结合实际情况灵活应用,不要机械照搬
4. 规约会随着技术发展不断更新,建议关注最新版本
5. 对于团队已有规范的情况,应以团队规范为准

## 🤝 贡献

本项目是将PDF文档转换为Skills的工具项目。如果你发现内容问题或有改进建议，欢迎提出。

## 📜 许可证

本Skills内容来源于《阿里巴巴Java开发手册》，遵循原文档的版权声明。

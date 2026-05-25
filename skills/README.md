# Alibaba Java Coding Guidelines Skills

This project converts the "Alibaba Java Coding Guidelines (Huangshan Edition)" PDF into universal AI Agent Skills,
supporting multiple AI/IDE platforms (Claude, Codex, Cursor, etc.), making it easy to quickly reference and apply Java
development guidelines during development.

## 📚 Project Overview

The Skills in this project are based on the "Java Development Guidelines (Huangshan Edition)" written by Alibaba Group's
technical team. This manual is the结晶 of collective wisdom and experience summary from the Java community, having
undergone multiple large-scale frontline practical tests and continuous improvements. The manual takes a Java
developer-centric perspective, divided into seven dimensions, further subdivided into secondary subdirectories based on
content characteristics.

## 🎯 Manual Vision

**Code Efficiently, Code with Quality**

The complexity of modern software architecture requires collaborative development. Appropriate norms and standards are
by no means meant to eliminate the creativity and elegance of code, but rather to limit excessive personalization. By
working together in a universally accepted unified way, we can improve collaboration efficiency and reduce communication
costs.

## 🎯 Cross-Platform Compatibility

The Skills in this project adopt the **unified SKILL.md format standard**, supporting multiple AI/IDE platforms (Claude,
Codex, Cursor, etc.).

## 📁 Skills Directory Structure

```
skills/
├── java-coding-standards/        # Coding Standards (Universal)
│   └── SKILL.md
├── java-exception-logging/       # Exception & Logging (Universal)
│   └── SKILL.md
├── java-unit-testing/            # Unit Testing (Universal)
│   └── SKILL.md
├── java-security-standards/      # Security Standards (Universal)
│   └── SKILL.md
├── java-mysql-database/          # MySQL Database (Universal)
│   └── SKILL.md
├── java-project-structure/       # Project Structure (Universal)
│   └── SKILL.md
├── java-design-standards/        # Design Standards (Universal)
│   └── SKILL.md
├── README.md                     # English documentation
└── README.zh.md                  # Chinese documentation
```

## 🚀 How to Use

### Installing Skills

Use the following commands to install the required Skills:

```bash
# View all available Skills
npx skills add https://github.com/millet0328/Alibaba-Java-Coding-Guidelines --list

# Install a single Skill
npx skills add https://github.com/millet0328/Alibaba-Java-Coding-Guidelines --skill java-coding-standards

# Install multiple specific Skills
npx skills add https://github.com/millet0328/Alibaba-Java-Coding-Guidelines --skill java-coding-standards java-exception-logging java-mysql-database

# Install all Skills at once (Recommended)
npx skills add https://github.com/millet0328/Alibaba-Java-Coding-Guidelines
```

### Cross-Platform Usage

These Skills adopt a unified format and can be automatically recognized and loaded by multiple AI/IDE platforms:

- **Claude** - Claude Desktop / Claude.ai
- **Codex** - OpenAI Codex
- **Cursor** - Cursor IDE
- And other AI Agent platforms that support SKILL.md format

### Automatic Triggering

When you are writing Java code, the AI will automatically activate relevant Skills based on the context to provide you
with convention suggestions.

### Manual Triggering

You can also use it in the following ways:

1. **During Code Review** - Ask AI assistant: "Please check this code according to Alibaba Java Coding Guidelines"
2. **When Writing Code** - Ask AI assistant: "How to name this class according to Alibaba conventions?"
3. **When Designing Database** - Ask AI assistant: "Is this table design reasonable according to MySQL conventions?"

### Example Conversation

```
User: How to name a user service class?
AI Assistant: According to Alibaba Java Coding Guidelines programming conventions, class names use UpperCamelCase style...
```

```
User: Does this exception handling code comply with standards?
AI Assistant: According to exception and logging conventions, it is recommended to use...
```

## 📖 Skills List

### 1. java-coding-standards

**Description:** Alibaba Java Coding Guidelines for programming conventions, including naming styles, constant
definitions, code formatting, OOP conventions, date/time handling, collection processing, concurrency, control
statements, comment conventions, etc.

**Use Cases:**

- When writing Java code
- During code review
- When following Alibaba Java coding standards

**Main Content:**

- (1) Naming Style - Class names, method names, variable names conventions
- (2) Constant Definitions - Constant definition and usage conventions
- (3) Code Format - Code formatting, indentation, line breaks conventions
- (4) OOP Conventions - Object-oriented programming conventions
- (5) Date/Time - Date and time handling conventions
- (6) Collection Processing - Collection class usage conventions
- (7) Concurrency - Multithreading and concurrent programming conventions
- (8) Control Statements - if/for/while control statement conventions
- (9) Comment Conventions - Code comment conventions
- (10) Frontend/Backend - Frontend-backend interaction conventions
- (11) Others - Other programming conventions

### 2. java-exception-logging

**Description:** Alibaba Java Coding Guidelines for exception and logging conventions, including error codes, exception
handling, and logging conventions.

**Use Cases:**

- When handling exceptions
- When writing logging code
- When designing error code systems

**Main Content:**

- (1) Error Codes - Error code design principles and conventions
- (2) Exception Handling - Exception catching and handling conventions
- (3) Logging Conventions - Log recording and output conventions

### 3. java-unit-testing

**Description:** Alibaba Java Coding Guidelines for unit testing conventions.

**Use Cases:**

- When writing unit tests
- When writing test cases
- When testing Java code

**Main Content:**

- AIR principles (Automatic, Independent, Repeatable)
- Unit test writing conventions
- Test case design conventions
- Mock and Stub usage conventions

### 4. java-security-standards

**Description:** Alibaba Java Coding Guidelines for security conventions.

**Use Cases:**

- When implementing security features
- When handling authentication and authorization
- When applying security best practices

**Main Content:**

- Permission control verification
- Sensitive data masking
- SQL injection prevention
- XSS prevention
- Parameter validation
- Other security conventions

### 5. java-mysql-database

**Description:** Alibaba Java Coding Guidelines for MySQL database conventions, including table design, index
conventions, SQL statements, and ORM mapping.

**Use Cases:**

- When designing database architecture
- When writing SQL queries
- When working with MySQL

**Main Content:**

- (1) Table Design - Database table design conventions
- (2) Index Conventions - Index design and optimization conventions
- (3) SQL Statements - SQL writing conventions
- (4) ORM Mapping - ORM framework usage conventions

### 6. java-project-structure

**Description:** Alibaba Java Coding Guidelines for project structure conventions, including application layering,
second-party library dependencies, and server configuration.

**Use Cases:**

- When building Java project structure
- When managing dependencies
- When organizing project architecture

**Main Content:**

- (1) Application Layering - Application layered architecture conventions
- (2) Second-Party Library Dependencies - Dependency management conventions
- (3) Server - Server configuration conventions

### 7. java-design-standards

**Description:** Alibaba Java Coding Guidelines for design conventions.

**Use Cases:**

- When designing software architecture
- When applying design patterns
- When making design decisions

**Main Content:**

- Storage solutions and data structure design
- Requirements analysis (use case diagrams, state diagrams, sequence diagrams, class diagrams, activity diagrams)
- System dependency design
- Other design conventions

## 🔍 Convention Categories

Conventions in the manual are divided into three categories based on constraint strength and fault sensitivity:

- **[MANDATORY]** - Must be strictly followed, violations may lead to serious issues
- **[RECOMMENDED]** - Suggested to follow, helps improve code quality
- **REFERENCE** - Reference suggestions, can be chosen based on actual situations

## 📝 Convention Description Format

Each convention entry includes the following information:

- **Explanation** - Appropriate expansion and interpretation of the convention
- **Positive Example** - Recommended coding and implementation approaches
- **Negative Example** - Pitfalls to avoid and real error cases

## 📊 Statistics

- **总Skills数量:** 7个(通用格式)
- **SKILL.md格式:** 统一标准,跨平台兼容
- **原PDF页数:** 55页
- **版本:** 黄山版(1.7.1)
- **更新日期:** 2022.02.03
- **重构日期:** 2024年5月25日(合并为通用skill)

## 📄 内容来源

- **原始文档：** 《Java开发手册（黄山版）》
- **制定团队：** 全球Java社区开发者
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

## 🔄 版本历史

- **2024-05-25** - 重构为通用skill格式,删除平台特定副本(.claude/、.codex/、.cursor/)
- **2024年初** - 初始版本,创建平台特定的skill副本

## 🤝 贡献

本项目是将PDF文档转换为Skills的工具项目。如果你发现内容问题或有改进建议，欢迎提出。

## 📜 许可证

本Skills内容来源于《阿里巴巴Java开发手册》，遵循原文档的版权声明。

---

**最后更新：** 2024年

**维护者：** 项目团队

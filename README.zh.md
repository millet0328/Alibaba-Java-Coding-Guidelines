# P3C - 阿里巴巴Java开发手册

**最新版本：** 黄山版 (发布日期 2022-02-03)

[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

## 前言

> 我们很高兴向大家展示阿里巴巴Java开发手册，该手册凝聚了阿里巴巴集团技术团队多年来在编程实践方面的最佳实践。随着项目数量的增长，我们鼓励代码复用并更好地理解彼此的程序，这对Java编程团队的代码质量提出了更高的要求。我们过去见过很多编程问题，例如：有缺陷的数据库表结构和索引设计可能导致软件架构缺陷和性能风险；混乱的代码结构难以维护；此外，没有身份验证的脆弱代码容易受到黑客攻击。为了解决这类问题，我们为阿里巴巴的Java开发者编写了本文档。

## 文档

- **中文版**: 下载 [Java开发手册(黄山版).pdf](Java开发手册(黄山版).pdf)
- **英文版**: [Alibaba Java Coding Guidelines](https://alibaba.github.io/Alibaba-Java-Coding-Guidelines)

## 项目组件

本项目由**4个主要部分**组成：

1. **[PMD实现](p3c-pmd)** - 基于PMD的静态代码分析插件
   - 实现了53条基于PMD的规则
   - 用于代码扫描的命令行工具
   - 支持CI/CD集成

2. **[IntelliJ IDEA插件](idea-plugin)** - JetBrains IDE的IDE插件
   - 实时代码检查
   - 快速修复建议
   - 与IDEA检查框架集成

3. **[Eclipse插件](eclipse-plugin)** - Eclipse的IDE插件
   - 实时代码检查
   - 快速修复建议
   - 与Eclipse标记框架集成

4. **[AI Agent Skills](skills/)** - AI编程助手
   - 7个通用AI/IDE平台技能(Claude、Codex、Cursor等)
   - 基于SKILL.md标准格式
   - 跨平台兼容
   - 详情请见 [skills/README.zh.md](skills/README.zh.md)

## 插件特性

### 基于PMD的规则(53条规则)

所有规则都在 [p3c-pmd README](p3c-pmd/README.md) 中有详细说明。主要类别包括：

- 编程规约(命名、常量、代码格式)
- OOP实践(equals、hashCode、POJO设计)
- 集合处理
- 并发控制
- 异常和日志标准
- 数据库和SQL标准
- 安全实践

### IDE插件额外规则(4条规则)

这4条规则直接在IDE插件(IDEA和Eclipse)中实现：

1. **【强制】禁止使用已废弃的类或方法。**
   - 示例：使用 `decode(String source, String encode)` 替代已废弃的 `decode(String encodeStr)`
   - 当接口被废弃时，提供者必须提供替代方案。程序员应该检查是否有新的实现。

2. **【强制】覆写的方法必须包含@Override注解。**
   - 反例：`getObject()` vs `get0bject()` (字母O与数字0)
   - `@Override` 注解确保正确覆写并在编译时捕获签名更改。

3. **【强制】静态字段/方法必须通过类名访问，而不是对象实例。**
   - 直接访问提高代码清晰度并避免混淆。

4. **【强制】hashCode和equals必须遵循以下规则：**
   - 如果覆写了`equals`，则必须覆写`hashCode`
   - 对于`Set`防止重复，两个方法都必须被覆写
   - 对于自定义`Map`键，两个方法都必须被覆写
   - 注意：`String`可以作为`Map`键使用，因为这些方法已经实现

## AI Agent Skills

本项目现在包含**7个通用AI Agent Skills**用于跨平台支持：

### Skills概览

| Skill | 描述 | 行数 |
|-------|-------------|-------|
| [java-coding-standards](skills/java-coding-standards/) | 编程规约(命名、OOP、集合、并发) | 1019 |
| [java-design-standards](skills/java-design-standards/) | 设计原则和模式 | 347 |
| [java-exception-logging](skills/java-exception-logging/) | 异常处理和日志标准 | 177 |
| [java-mysql-database](skills/java-mysql-database/) | MySQL数据库设计和SQL标准 | 185 |
| [java-project-structure](skills/java-project-structure/) | 项目结构和依赖管理 | 115 |
| [java-security-standards](skills/java-security-standards/) | 安全最佳实践 | 44 |
| [java-unit-testing](skills/java-unit-testing/) | 单元测试原则(AIR框架) | 65 |

**总计：** 7个skills，1952行全面的指南

### 平台支持

这些skills使用统一的**SKILL.md格式**并兼容**所有支持SKILL.md的平台**，包括但不限于：
- Claude Desktop / Claude.ai
- OpenAI Codex
- Cursor IDE
- Qoder
- 以及其他支持SKILL.md标准的AI Agent平台

## 使用方法

关于每个组件的详细文档和使用说明，请参考各自的README文件：

- **PMD插件**: [p3c-pmd/README.md](p3c-pmd/README.md)
- **IDEA插件**: [idea-plugin/README.md](idea-plugin/README.md)
- **Eclipse插件**: [eclipse-plugin/README.md](eclipse-plugin/README.md)
- **AI Skills**: [skills/README.zh.md](skills/README.zh.md)

## 贡献

我们欢迎贡献！详情请参阅我们的[贡献指南](.github/ISSUE_TEMPLATE/)。

- 通过[Issue模板](.github/ISSUE_TEMPLATE/)报告bug
- 建议新规则
- 改进现有实现

## 许可证

基于Apache许可证2.0版授权。详情请参阅 [LICENSE](license.txt)。

## 相关资源

- [官方网站](https://developer.aliyun.com/special/tech-java)
- [配套图书《码出高效》](https://developer.aliyun.com/special/tech-java)
- [GitHub仓库](https://github.com/alibaba/p3c)

---

**使命：** 码出高效，码出质量。Code efficiently, code with quality.

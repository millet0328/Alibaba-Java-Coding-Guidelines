# P3C - Alibaba Java Coding Guidelines

**Latest Version:** Huangshan Edition (Released 2022-02-03)

[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

## Preface

> We are pleased to present Alibaba Java Coding Guidelines which consolidates the best programming practices over the years from Alibaba Group's technical teams. A vast number of Java programming teams impose demanding requirements on code quality across projects as we encourage reuse and better understanding of each other's programs. We have seen many programming problems in the past. For example, defective database table structures and index designs may cause software architecture flaws and performance risks. Another example is confusing code structures being difficult to maintain. Furthermore, vulnerable code without authentication is prone to hackers' attacks. To address these kinds of problems, we developed this document for Java developers at Alibaba.

## Documentation

- **中文版**: 下载 [Java开发手册(黄山版).pdf](Java开发手册(黄山版).pdf)
- **English Version**: [Alibaba Java Coding Guidelines](https://alibaba.github.io/Alibaba-Java-Coding-Guidelines)

## Project Components

This project consists of **4 main parts**:

1. **[PMD Implementations](p3c-pmd)** - PMD-based static code analysis plugin
   - 53 rules implemented based on PMD
   - Command-line tool for code scanning
   - CI/CD integration support

2. **[IntelliJ IDEA Plugin](idea-plugin)** - IDE plugin for JetBrains IDEs
   - Real-time code checking
   - Quick-fix suggestions
   - Integration with IDEA inspection framework

3. **[Eclipse Plugin](eclipse-plugin)** - IDE plugin for Eclipse
   - Real-time code checking
   - Quick-fix suggestions
   - Integration with Eclipse marker framework

4. **[AI Agent Skills](skills/)** - AI-powered coding assistants
   - 7 universal skills for AI/IDE platforms (Claude, Codex, Cursor, etc.)
   - Based on SKILL.md standard format
   - Cross-platform compatibility
   - See [skills/README.zh.md](skills/README.zh.md) for details (Chinese)

## Plugin Features

### PMD-Based Rules (53 rules)

All rules are documented in the [p3c-pmd README](p3c-pmd/README.md). Key categories include:

- Programming conventions (naming, constants, code format)
- OOP practices (equals, hashCode, POJO design)
- Collection handling
- Concurrency control
- Exception and logging standards
- Database and SQL standards
- Security practices

### IDE Plugin Additional Rules (4 rules)

These 4 rules are implemented directly in the IDE plugins (IDEA and Eclipse):

1. **[Mandatory] Using a deprecated class or method is prohibited.**
   - Example: Use `decode(String source, String encode)` instead of deprecated `decode(String encodeStr)`
   - When an interface is deprecated, the provider must offer a replacement. Programmers should check for new implementations.

2. **[Mandatory] Overridden methods must include @Override annotation.**
   - Counter example: `getObject()` vs `get0bject()` (letter O vs number 0)
   - The `@Override` annotation ensures correct overriding and catches signature changes at compile time.

3. **[Mandatory] Static fields/methods must be accessed via class name, not object instances.**
   - Direct access improves code clarity and avoids confusion.

4. **[Mandatory] hashCode and equals must follow these rules:**
   - Override `hashCode` if `equals` is overridden
   - Both methods must be overridden for `Set` to prevent duplicates
   - Both methods must be overridden for custom `Map` keys
   - Note: `String` can be used as `Map` key since these methods are already implemented

## AI Agent Skills

The project now includes **7 universal AI Agent Skills** for cross-platform support:

### Skills Overview

| Skill | Description | Lines |
|-------|-------------|-------|
| [java-coding-standards](skills/java-coding-standards/) | Programming conventions (naming, OOP, collections, concurrency) | 1019 |
| [java-design-standards](skills/java-design-standards/) | Design principles and patterns | 347 |
| [java-exception-logging](skills/java-exception-logging/) | Exception handling and logging standards | 177 |
| [java-mysql-database](skills/java-mysql-database/) | MySQL database design and SQL standards | 185 |
| [java-project-structure](skills/java-project-structure/) | Project structure and dependency management | 115 |
| [java-security-standards](skills/java-security-standards/) | Security best practices | 44 |
| [java-unit-testing](skills/java-unit-testing/) | Unit testing principles (AIR framework) | 65 |

**Total:** 7 skills, 1952 lines of comprehensive guidelines

### Platform Support

These skills use the unified **SKILL.md format** and work with **all platforms that support SKILL.md**, including but not limited to:
- Claude Desktop / Claude.ai
- OpenAI Codex
- Cursor IDE
- Qoder
- And any other AI Agent platforms supporting the SKILL.md standard

## Usage

For detailed documentation and usage instructions for each component, please refer to their respective README files:

- **PMD Plugin**: [p3c-pmd/README.md](p3c-pmd/README.md)
- **IDEA Plugin**: [idea-plugin/README.md](idea-plugin/README.md)
- **Eclipse Plugin**: [eclipse-plugin/README.md](eclipse-plugin/README.md)
- **AI Skills**: [skills/README.zh.md](skills/README.zh.md)

## Contributing

We welcome contributions! Please see our [Contributing Guide](.github/ISSUE_TEMPLATE/) for details.

- Report bugs via [Issue Templates](.github/ISSUE_TEMPLATE/)
- Suggest new rules
- Improve existing implementations

## License

Licensed under the Apache License, Version 2.0. See [LICENSE](license.txt) for details.

## Related Resources

- [Official Website](https://developer.aliyun.com/special/tech-java)
- [Companion Book: "Code Efficiently"](https://developer.aliyun.com/special/tech-java)
- [GitHub Repository](https://github.com/alibaba/p3c)

---

**Mission:** Code efficiently, code with quality. 码出高效，码出质量。


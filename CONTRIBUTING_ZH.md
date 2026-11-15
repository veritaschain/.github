# VeritasChain Protocol 贡献指南

感谢您有兴趣为 VeritasChain Protocol（VCP）做出贡献！本文档提供贡献的指南和说明。

## 目录

- [行为准则](#行为准则)
- [如何贡献](#如何贡献)
- [入门](#入门)
- [开发工作流程](#开发工作流程)
- [风格指南](#风格指南)
- [提交消息](#提交消息)
- [拉取请求流程](#拉取请求流程)
- [社区](#社区)

## 行为准则

本项目及所有参与者均受我们的[行为准则](CODE_OF_CONDUCT_ZH.md)约束。参与即表示您同意遵守此准则。请将不可接受的行为报告至 info@veritaschain.org。

## 如何贡献

### 报告错误

在创建错误报告之前，请检查现有问题以避免重复。创建错误报告时，请包含尽可能多的详细信息：

- **使用清晰、描述性的标题**
- **描述重现问题的确切步骤**
- **提供具体示例**（代码片段、配置文件）
- **描述您观察到的行为以及您期望的行为**
- **包含相关日志和错误消息**

### 建议增强功能

欢迎增强功能建议！请提供：

- **清晰、描述性的标题**
- **对建议增强功能的详细描述**
- **解释为什么此增强功能会有用**
- **列出您考虑过的任何替代方案**

### 贡献代码

我们欢迎代码贡献！您可以帮助的领域：

- **错误修复** - 修复报告的问题
- **文档** - 改进或翻译文档
- **测试** - 添加或改进测试覆盖率
- **功能** - 实现新功能（请先讨论）

### 改进文档

文档改进始终受欢迎：

- 修复拼写和语法错误
- 添加缺失的信息
- 提高清晰度和可读性
- 翻译文档（支持 EN、JA、ZH）

## 入门

### 先决条件

请以目标存储库的 README、贡献指南和运行环境声明为准，确认支持的版本。
项目可能使用以下工具：

- **Node.js** 和 npm（用于 TypeScript；检查 `package.json` 的 engines 和 `.nvmrc`）
- **Python**（检查 `pyproject.toml` 的 `requires-python` 或该存储库的要求）
- **MetaTrader 5**（用于 MQL5 项目）
- **Git** 用于版本控制

例如，[Explorer API](https://github.com/veritaschain/vcp-explorer-api#quick-start)和
[Explorer GUI](https://github.com/veritaschain/vcp-explorer-gui#prerequisites)各自公布运行环境要求。
[SDK](https://github.com/veritaschain/vcp-sdk#install)分别提供 Python、TypeScript 和 MQL5 的安装说明。

### Fork 和克隆

1. 在 GitHub 上 Fork 存储库
2. 在本地克隆您的 Fork：
   ```bash
   git clone https://github.com/您的用户名/存储库名称.git
   cd 存储库名称
   ```
3. 添加上游远程：
   ```bash
   git remote add upstream https://github.com/veritaschain/存储库名称.git
   ```

### 安装依赖

请按目标存储库的安装说明，在指定的包目录中操作。
对于提交了锁文件的 npm 项目，使用其文档规定的 `npm ci` 流程。
Python 项目可能使用 requirements 文件，也可能使用带测试 extras 的可安装 `pyproject.toml` 包；
请采用该存储库定义的方式。纯文档存储库可能没有运行时依赖。

## 开发工作流程

### 创建分支

为您的更改创建分支：

```bash
git checkout -b feature/您的功能名称
# 或
git checkout -b fix/问题描述
```

分支命名约定：
- `feature/` - 新功能
- `fix/` - 错误修复
- `docs/` - 文档更改
- `refactor/` - 代码重构
- `test/` - 测试添加或修改

### 进行更改

1. 在您的分支中进行更改
2. 根据需要编写或更新测试
3. 确保所有测试通过
4. 必要时更新文档

### 测试

请运行目标存储库的贡献指南和 CI 定义的检查。
在 npm 包目录中，`npm run` 会列出实际存在的脚本；lint、类型检查以及测试前的构建要求因项目而异。
对于 Python，请安装文档指定的测试依赖，并使用该项目的测试运行器。
如果存储库提供链接检查或文档构建，请使用这些检查验证文档。

## 风格指南

### TypeScript/JavaScript

- 使用 **ESLint** 和 **Prettier** 进行格式化
- 使用 TypeScript 严格模式
- 优先使用 `const` 而非 `let`
- 使用有意义的变量和函数名
- 为公共 API 添加 JSDoc 注释

```typescript
/**
 * 使用指定参数创建新的 VCP 事件。
 * @param eventType - 事件类型（SIG、ORD、EXE 等）
 * @param payload - 事件负载
 * @returns 创建的 VCP 事件
 */
export function createEvent(eventType: EventType, payload: Payload): VcpEvent {
  // 实现
}
```

### Python

- 遵循 **PEP 8** 风格指南
- 使用 **Black** 进行格式化
- 为函数签名使用**类型提示**
- 为公共函数添加文档字符串

```python
def create_event(event_type: str, payload: dict) -> VcpEvent:
    """
    使用指定参数创建新的 VCP 事件。

    Args:
        event_type: 事件类型（SIG、ORD、EXE 等）
        payload: 事件负载

    Returns:
        创建的 VCP 事件
    """
    # 实现
```

### MQL5

- 使用描述性变量名
- 为复杂逻辑添加注释
- 遵循 MetaQuotes 编码标准

### 文档

- 文档使用 **Markdown**
- 保持合理的行长度（≤120 字符）
- 使用标题组织内容
- 在有帮助的地方包含代码示例

## 提交消息

我们遵循 [Conventional Commits](https://www.conventionalcommits.org/) 规范：

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

### 类型

- `feat` - 新功能
- `fix` - 错误修复
- `docs` - 文档更改
- `style` - 代码风格更改（格式化等）
- `refactor` - 代码重构
- `test` - 添加或修改测试
- `chore` - 维护任务
- `ci` - CI/CD 更改

### 示例

```
feat(sdk): 添加用于 VCP 事件记录的 Python SDK

fix(explorer): 解决 Merkle 证明验证错误

docs(readme): 添加日语快速入门部分

ci: 添加用于自动化测试的 GitHub Actions 工作流
```

## 拉取请求流程

### 提交前

1. **使用最新的上游更改更新您的分支**：
   ```bash
   git fetch upstream
   git rebase upstream/main
   ```

2. **确保所有检查通过**：
   - 所有测试通过
   - 代码遵循风格指南
   - 文档已更新

3. **编写清晰的 PR 描述**：
   - 做了哪些更改
   - 为什么做这些更改
   - 相关问题（持续进行的工作使用 `Refs #123`；仅当整个问题已解决时使用自动关闭关键词）

### 审查流程

1. 维护者将审查您的 PR
2. 处理任何请求的更改
3. 批准后，维护者将合并您的 PR

### 合并后

- 删除您的功能分支
- 从上游拉取最新更改

## 社区

### 获取帮助

- **GitHub Issues** - 用于错误和功能请求
- **GitHub Discussions** - 用于问题和一般讨论
- **电子邮件** - info@veritaschain.org

### 保持联系

- **网站**：https://veritaschain.org
- **GitHub**：https://github.com/veritaschain
- **LinkedIn**：https://linkedin.com/company/110199945

---

## 致谢

贡献者将在我们的发布说明和网站上得到认可。感谢您帮助使 VCP 变得更好！

---

<p align="center">
  <strong>VeritasChain Standards Organization</strong><br/>
  <em>"Verify, Don't Trust"</em>
</p>

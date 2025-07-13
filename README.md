# Obsidian 示例插件

这是一个 Obsidian 的示例插件(https://obsidian.md)

该项目使用 TypeScript 提供类型检查和文档支持。
该仓库依赖于 TypeScript 定义格式下的最新插件 API（obsidian.d.ts），其中包含描述其功能的 TSDoc 注释。

此示例插件演示了插件 API 能够实现的一些基本功能。
- 添加一个 ribbon 图标，点击后显示一个通知。
- 添加一个命令“打开示例模态窗口”，该命令会打开一个模态窗口。
- 在设置页面中添加一个插件设置选项卡。
- 注册全局点击事件，并在控制台输出“click”。
- 注册一个全局间隔事件，并在控制台输出“setInterval”。

## 首次开发插件？

新插件开发者的快速入门指南：

- 检查是否已有其他人开发了您需要的插件（https://obsidian.md/plugins）！可能已有足够相似的现有插件，您可以与之合作。
- 使用“使用此模板”按钮将此仓库克隆为模板（如果看不到该按钮，请登录 GitHub）。
- 将仓库克隆到本地开发文件夹。为了方便，你可以将此文件夹放在 `.obsidian/plugins/your-plugin-name` 文件夹中。
- 安装 NodeJS，然后在仓库文件夹下的命令行中运行 `npm i`。
- 运行 `npm run dev` 以将 `main.ts` 编译为 `main.js`。
- 对 `main.ts` 文件进行修改（或创建新的 `.ts` 文件）。这些修改将自动编译为 `main.js`。
- 重新加载 Obsidian 以加载插件的新版本。
- 在设置窗口中启用插件。
- 若需更新 Obsidian API，请在仓库文件夹下的命令行中运行 `npm update`。

## 发布新版本

- 在 `manifest.json` 中更新您的版本号，例如 `1.0.1`，以及您最新版本所需的最低 Obsidian 版本。
- 在 `versions.json` 文件中添加 `"new-plugin-version": "minimum-obsidian-version"`，以便旧版本的 Obsidian 可以下载与之兼容的旧版本插件。
- 使用新版本号作为“标签版本”创建新的 GitHub 发布版本。请使用确切的版本号，不要包含前缀 `v`。示例请参见：https://github.com/obsidianmd/obsidian-sample-plugin/releases
- 将文件 `manifest.json`、`main.js`、`styles.css` 作为二进制附件上传。注意：`manifest.json` 文件必须放在两个位置，首先是仓库的根路径，其次是在发布版本中。
- 发布版本。

> 您可以通过在手动更新 `manifest.json` 中的 `minAppVersion` 后运行 `npm version patch`、`npm version minor` 或 `npm version major` 来简化版本更新流程。
> 该命令将更新 `manifest.json` 和 `package.json` 中的版本号，并向 `versions.json` 中添加新版本的条目。

## 将您的插件添加到社区插件列表

- 查看 [插件指南](https://docs.obsidian.md/Plugins/Releasing/Plugin+guidelines)。
- 发布初始版本。
- 确保您的仓库根目录下有一个 `README.md` 文件。
- 通过 https://github.com/obsidianmd/obsidian-releases 提交拉取请求以添加您的插件。

## 使用方法

- 克隆此仓库。
- 确保您的 NodeJS 版本至少为 v16（使用 `node --version` 命令检查）。
- 使用 `npm i` 或 `yarn` 安装依赖项。
- 运行 `npm run dev` 以启动监听模式下的编译。

## 手动安装插件

- 将 `main.js`、`styles.css` 和 `manifest.json` 复制到你的 Vault 目录 `VaultFolder/.obsidian/plugins/your-plugin-id/` 中。

## 使用 ESLint 提升代码质量（可选）
- [ESLint](https://eslint.org/) 是一款用于分析代码并快速发现问题的工具。您可以运行 ESLint 检查插件，以发现常见问题并改进代码质量。 
- 要在此项目中使用 ESLint，请确保通过终端安装 ESLint：
  - `npm install -g eslint`
- 要使用 ESLint 分析此项目，请使用以下命令：
  - `eslint main.ts`
  - ESLint 将生成一份报告，按文件和行号提供代码改进建议。
- 如果您的源代码位于某个文件夹中（例如 `src`），您可以使用以下命令对该文件夹中的所有文件进行分析：
  - `eslint .\src\`

## 资金链接

您可以添加资金链接，以便使用您插件的人可以对它进行财务支持。

最简单的方法是在 `manifest.json` 文件中将 `fundingUrl` 字段设置为您的链接：

```json
{
    "fundingUrl": "https://buymeacoffee.com"
}
```

如果你有多个URL，你也可以这样做：

```json
{
    "fundingUrl": {
        "Buy Me a Coffee": "https://buymeacoffee.com",
        "GitHub 赞助": "https://github.com/sponsors",
        "Patreon": "https://www.patreon.com/"
    }
}
```

## API 文档

参见 https://github.com/obsidianmd/obsidian-api


通过DeepL翻译 (https://dee.pl/app)

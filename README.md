# VSCode Angular Expansion

#### 包含扩展的简要说明

- **Angular 10 Snippets** - Angular10 代码片段
- **Angular File Help** - 快捷创建 Angular 文件
- **Angular Language Service** - Angular 语言支持服务
- **Auto Close Tag** - 自动闭合 html 标签
- **Auto Rename Tag** - 自动重命名 html 标签
- **Bracket Pair Colorizer** - 使用颜色标识匹配括号
- **Chinese (Simplified) Language Pack for Visual Studio Code** - 中文（简体）语言包扩展
- **Code Runner** - 一个与 camelCase 代码配合良好的基本拼写检查程序
- **GitLens** - 增强 Visual Studio 代码内置的 Git 功能
- **Import Cost** - 在编辑器中显示导入/需要包大小
- **Live Server** - html 快捷服务器
- **Markdown Preview Enhanced** - Markdown 预览增强
- **NG-ZORRO Snippets** - npm 支持 VS Code
- **npm Intellisense** - 用于在 import 语句中自动填充 npm 模块
- **Path Intellisense** - 自动填充文件名
- **formate: CSS/LESS/SCSS formatter** - 样式文件格式化工具
- **Prettier** - 格式化您的 JavaScript / TypeScript / CSS
- **TODO Highlight** - 突出显示 TODO，FIXME 和任何关键字，注释......
- **Todo Tree** - 管理代码中自定义任务标识
- **Turbo Console Log** - 快捷打印代码中的变量
- **vscode-fileheader** - 插入标题注释，并自动更新时间
- **VS Code Counter** - 项目代码量统计
- **vscode-icons** - Visual Studio 代码的图标
- **Web-Dev-Snippets** - Web 开发代码片段集合
- **Yapi File Help** - Yapi 接口信息生成工具

#### 将这些推荐设置粘贴到 VS 代码工作区设置中，以增强您的 vs 代码。

```json
{
  // 启动页
  "workbench.startupEditor": "newUntitledFile",
  // 编辑器失去焦点时自动保存更新后的文件
  "files.autoSave": "onFocusChange",
  // 以像素为单位控制字体大小
  "editor.fontSize": 16,
  // 粘贴时进行格式化
  "editor.formatOnPaste": true,
  // 路径提示映射
  "path-intellisense.mappings": {
    "@": "${workspaceRoot}/src"
  },
  // 高亮注释关键字
  "todohighlight.keywords": [
    {
      "text": "@Author",
      "color": "#000",
      "backgroundColor": "#808695"
    },
    {
      "text": "@Date",
      "color": "#000",
      "backgroundColor": "#c5c8ce"
    },
    {
      "text": "@Last Modified by",
      "color": "#000",
      "backgroundColor": "#dcdee2"
    },
    {
      "text": "@Last Modified time",
      "color": "#000",
      "backgroundColor": "#e8eaec"
    },
    {
      "text": "@Description",
      "color": "#000",
      "backgroundColor": "#f8f8f9"
    }
  ],
  // 注释高亮默认注释
  "todohighlight.defaultStyle": {
    "fontWeight": "5000",
    "color": "#000",
    "backgroundColor": "#0dbc79",
    "cursor": "pointer",
    "border": "0px solid #eee",
    "borderRadius": "0px",
    "letterSpacing ": "2px",
    "isWholeLine": false
  },
  // 是否启用注释高亮
  "todohighlight.isEnable": true,
  // 创建文件的用户名
  "fileheader.Author": "Sun Rising",
  // 更新文件的用户名
  "fileheader.LastModifiedBy": "Sun Rising",
  // 文件头注释模板
  "fileheader.tpl": "/**\r\n * @Author: {author} \r\n * @Date: {createTime} \r\n * @Description: \r\n */\r\n",
  // 图标主题
  "workbench.iconTheme": "vscode-icons",
  // 禁用软件后台更新
  "update.enableWindowsBackgroundUpdates": false,
  // 禁止检查扩展更新
  "extensions.autoCheckUpdates": false,
  // 禁止扩展自动更新
  "extensions.autoUpdate": false,
  // 控制是否在键入时自动显示建议
  "editor.quickSuggestions": {
    "strings": true
  },
  // 控制活动代码段是否阻止快速建议
  "editor.suggest.snippetsPreventQuickSuggestions": false,
  // 保存时禁止格式化
  "editor.formatOnSave": true,
  //markdown样式
  "markdown-preview-enhanced.codeBlockTheme": "atom-dark.css",
  //markdown字体
  "markdown.preview.fontFamily": "\"Microsoft YaHei\",-apple-system, BlinkMacSystemFont, \"Segoe UI\", Roboto, Helvetica, Arial, sans-serif, \"Apple Color Emoji\", \"Segoe UI Emoji\", \"Segoe UI Symbol\"",
  // 调试配置
  "launch": {
    "version": "0.2.0",
    "configurations": [
      {
        "type": "node",
        "request": "launch",
        "name": "Static : Node.js",
        "program": "${file}"
      },
      {
        "type": "chrome",
        "request": "launch",
        "name": "Static : Chrome",
        "file": "${file}",
        "webRoot": "${workspaceRoot}",
        // 非安装版 Chrome 浏览器执行文件地址
        // "runtimeExecutable": "C:/Program Files (x86)/Google/Chrome/Application/chrome.exe",
        "userDataDir": "${workspaceRoot}/.vscode/chrome"
      },
      {
        "type": "chrome",
        "request": "launch",
        "name": "Service : Chrome",
        "url": "http://localhost:8080",
        "webRoot": "${workspaceRoot}",
        "userDataDir": "${workspaceRoot}/.vscode/chrome"
      },
      {
        "type": "chrome",
        "request": "launch",
        "name": "Vue.js : Chrome",
        "url": "http://localhost:8080",
        "webRoot": "${workspaceFolder}/src",
        "breakOnLoad": true,
        "sourceMapPathOverrides": {
          "webpack:///./src/*": "${webRoot}/*",
          "webpack:///src/*": "${webRoot}/*",
          "webpack:///*": "*",
          "webpack:///./~/*": "${webRoot}/node_modules/*"
        }
      }
    ]
  },
  // 解决打开中文bat乱码的问题
  "[Batch]": {
    "files.encoding": "gbk"
  },
  // 程序启动不询问启动页
  "workbench.editor.untitled.hint": "hidden",
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[less]": {
    "editor.defaultFormatter": "MikeBovenlander.formate"
  }
}
```

#### 积分

- 感谢上述插件的原作者和贡献者。

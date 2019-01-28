# es6-runcode

vscode 右键 RunCode 直接运行 es6

```conf
// vscode 需要配置 Code Runner，`cmd + ,`
// codeRunner 需要全局安装一下模块
// sudo npm i eslint @babel/cli @babel/node @babel/preset-env prettier -g
// Error: Cannot find module '@babel/preset-env' from '/usr/local/lib' 报此错误需要改为当前项目为根目录再执行右键Run Code 或配置 `"code-runner.cwd": "/usr/local/lib/",`
{
  "code-runner.defaultLanguage": "javascript",
  "code-runner.cwd": "/usr/local/lib/",
  "code-runner.executorMap": {
    "vue": "babel-node",
    // babel 7
    "javascript": "npx babel-node --presets @babel/preset-env"
  }
}
```

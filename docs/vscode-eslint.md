# VSCode + ESLint配置

VSCode有内置的插件`eslint`可以标识出不符合规则的地方，并通过一些配置可以自动修复简单错误。

首先安装`eslint`插件
![eslint](https://wpimg.wallstcn.com/72f126cb-09eb-4b27-b02e-65e79eb76220.png)
然后点击 文件 > 首选项 > 设置 打开 VSCode 配置文件,添加如下配置
```json
{
  "files.autoSave": "off",
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "vue-html",
    {
      "language": "vue",
      "autoFix": true
    }
  ],
  "eslint.run": "onSave",
  "eslint.autoFixOnSave": true
}
```
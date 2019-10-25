# vue-cli3按需引入element-ui

vue-cli2按需引入element-ui可以参照[官网](https://element.eleme.cn/2.0/#/zh-CN/component/quickstart)，下面主要是vue-cli3的安装步骤：

- 下载 @babel/preset-env 和 babel-plugin-component
```
npm install @babel/preset-env babel-plugin-component -D
```
- 在babel.config.js文件内修改
```
module.exports = {
  presets: [
    "@vue/cli-plugin-babel/preset",  // 有可能值为'@vue/app'
    [
      '@babel/preset-env', {
        modules: false
      }
    ]
  ],
  plugins: [
    [
      'component',
      {
        'libraryName': 'element-ui',
        'styleLibraryName': 'theme-chalk'
      }
    ]
  ]
};
```


# xzq-gulp

## 安装

```shell
$ yarn add xzq-gulp --dev

# or npm
$ npm install xzq-gulp --save-dev
```

package.json可以配置 `scripts`:

```json
{
  "scripts": {
    "clean": "xzq-gulp clean",
    "serve": "xzq-gulp develop",
    "build": "xzq-gulp build",
  }
}
```
## 项目配置
在项目根目录下创建`pages.config.js`
```js
module.exports = {
  build: {    // 打包目录配置
    src: 'src',    // 入口
    dist: 'release',  // 出口
    temp: '.tmp',     // 临时运行文件
    public: 'public',  
    paths: {     // 打包文件地址配置
      styles: 'assets/styles/*.scss',
      scripts: 'assets/scripts/*.js',
      pages: '*.html',
      images: 'assets/images/**',
      fonts: 'assets/fonts/**'
    }
  },
  data: {},  // 工具中用到swig, 页面中需要传入的值放到data中
  serve: {   // 本地服务配置

  }
}
```

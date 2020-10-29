
> 是对项目或者模块包的描述。比如项目名称，项目版本，项目所需要的各种模块。npm install 命令会根据这个文件下载所有依赖模块。

## 示例
```
{
  "name": "vben-admin-2.0",
  "version": "2.0.0-rc.6",
  "scripts": {
    "serve": "esno ./build/script/preserve.ts && cross-env NODE_ENV=development vite",
    "build": "rimraf dist && cross-env NODE_ENV=production vite build && esno ./build/script/postBuild.ts"
  },
  "dependencies": {
    "ant-design-vue": "^2.0.0-beta.10",
    "vite": "^1.0.0-rc.8",
    "vue": "^3.0.2",
    "vue-router": "^4.0.0-rc.1",
    "vuex": "^4.0.0-beta.4"
  },
  "devDependencies": {
    "@types/koa-static": "^4.0.1",
    "@types/nprogress": "^0.2.0",
    "eslint": "^7.12.0",
    "eslint-plugin-vue": "^7.1.0",
    "husky": "^4.3.0",
    "koa-static": "^5.0.0",
    "less": "^3.12.2",
    "rollup-plugin-visualizer": "^4.1.2",
    "stylelint": "^13.7.2",
    "ts-node": "^9.0.0",
    "typescript": "^4.0.5"
  },
  "license": "MIT",
  "husky": {
    "hooks": {
      "pre-commit": "ls-lint && lint-staged",
      "commit-msg": "commitlint -E HUSKY_GIT_PARAMS"
    }
  },
  "engines": {
    "node": ">=10.16.1"
  }
}
```
## 相关配置说明
* name 项目/模块名称（必须）
* version 项目版本（必须）
* scripts 执行npm脚本命令简写，比如 scripts.serve, 执行 npm run serve 就是运行 "esno ./build/script/preserve.ts && cross-env NODE_ENV=development vite"。
* dependencies 生产环境下，项目运行所需模块
* devDependencies 开发环境下，项目运行所需模块
* engines 项目运行的平台
* private 是否私有，设置为 true 时，npm 拒绝发布
* license 软件授权条款，让用户知道他们的使用权利和限制
* bugs bug 提交地址
* repository 项目仓库地址
* homepage 项目包的官网 URL
* husky 提交前自动校验 可以在 commit 之前做代码校验，如果代码有格式问题，就会禁止提交
* browserslist 供浏览器使用的版本列表
* author 项目开发者
* escription 项目描述
* contributors 项目贡献者
* bin 内部命令对应的可执行文件的路径
* main 项目默认执行文件，比如 require(‘webpack’)；就会默认加载 lib 目录下的 webpack.js 文件，如果没有设置，则默认加载项目跟目录下的 index.js 文件
* module 是以 ES Module(也就是 ES6)模块化方式进行加载，因为早期没有 ES6 模块化方案时，都是遵循 CommonJS 规范，而 CommonJS 规范的包是以 main 的方式表示入口文件的，为了区分就新增了 module 方式，但是 ES6 模块化方案效率更高，所以会优先查看是否有 module 字段，没有才使用 main 字段
* eslintConfig EsLint 检查文件配置，自动读取验证

look at here [npm 官网 package.json说明](http://caibaojian.com/npm/files/package.json.html)
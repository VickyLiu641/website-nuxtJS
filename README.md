# xiaoha-website

## Build Setup

```bash
# 安装依赖  install dependencies
$ npm install

# 运行服务  serve with hot reload at localhost:8080
$ npm run dev

# 打包 build for production and launch server
$ npm run build
$ npm run start

# 生成静态项目 generate static project
$ npm run generate
```
## 技术选择

Nuxt.js 是一个基于 Vue.js 的通用应用框架。通过对客户端/服务端基础架构的抽象组织，Nuxt.js 主要关注的是应用的 UI 渲染。

**关于Nuxt与SSR**

利用 Nuxt的 SSR模式（也叫做 "universal" or "isomorphic" 模式），Node.js 服务器将基于 Vue 的组件渲染成 HTML 并传输到客户端，而不是纯 javascript。与传统的 Vue SPA 相比，使用 SSR 将带来巨大的 SEO 提升、更好的用户体验和更多的机会。

查看更多关于NuxtJS <br/>
For detailed explanation on how things work, check out the [documentation](https://nuxtjs.org).

**UI库**

https://vuetifyjs.com/zh-Hans/ <br/>
Vuetify 是建立在Vue.js之上的完备的界面框架。移动PC多端支持

**TypeScript**

https://www.tslang.cn/

## 插件

### vue-router 

```
npm i vue-router --save
```
### storejs

store.js 是一个兼容所有浏览器的 LocalStorage 包装器，不需要借助 Cookie 或者 Flash。store.js 会根据浏览器自动选择使用 localStorage、globalStorage 或者 userData 来实现本地存储功能。

https://www.npmjs.com/package/storejs

```
npm i storejs --save
```

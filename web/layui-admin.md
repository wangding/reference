# layui-admin pro SPA 框架

## 让 layui-admin 跑起来

- 修改 start/index.html
```html
<title>匠人牛品集团后台</title>
```

```javascript
layui.config({
  base: '../src'      // 这里本地开发用 src，线上用 dist
  ,version: '1.0.0-beta6'
}).use('index');

```

- 在 start 目录的上一级目录运行 lrd
- 浏览器访问地址：http://192.168.130.144:8080/start/

## 目录结构

- src/

layuiAdmin 源代码，通常用于开发环境（如本地），推荐你在本地开发时，将 ./start/index.html 中的 layui.css 和 layui.js 的引入路径由 dist 改为 src 目录。

  - src/controller/：存放 JS 业务模块，即对视图进行事件等交互性处理
  - src/lib/：layuiAdmin 的核心模块，一般不推荐修改
  - src/style/：存放样式，其中 admin.css 是核心样式
  - src/views/：存放视图文件。其中 layout.html 是整个框架结构的承载，一般不推荐做大量改动。
  - src/config.js：layuiAdmin 的全局配置文件，可随意修改。
  - src/index.js：layuiAdmin 的入口模块，一般不推荐修改

start/

存放 layuiAdmin 的入口页面、模拟接口数据、layui

dist/

通下面会介绍如何使用 gulp。过 gulp 将 layuiAdmin src 目录的源代码进行构建后生成的目录（即将JS 和 CSS 文件进行了压缩等处理），通常用于线上环境。

## 宿主页面

你所看到的 start/index.html 是我们提供好的宿主页面，它是整个单页面的承载，所有的界面都是在这一个页面中完成跳转和渲染的。事实上，宿主页面可以放在任何地方，但是要注意修改里面的 `<link> <script>` 的 src 和 layui.config 中 base 的路径。

## 全局配置

src/config.js，里面存储着所有的默认配置。可以按照实际需求选择性修改。

- 修改 config.js
```javascript
// 修改文件头注释
,name: '匠人牛品集团后台'
// 将来需要修改独立页面的路由，暂时不知道怎么修改
// 将来需要去掉调试模式：,debug: false
// 去掉主题配置
```

## 侧边菜单

在 start/json/menu.js 文件中，放置了侧边菜单数据，根据需要修改它。

## 路由

layuiAdmin 的路由是采用 location.hash 的机制，即路由地址是放在 ./#/ 后面，并通过 layui 自带的方法：layui.router() 来进行解析。每一个路由都对应一个真实存在的视图文件，且路由地址和视图文件的路径是一致的（相对 views 目录）。因此，你不再需要通过配置服务端的路由去访问一个页面，也无需在 layuiAdmin 内部代码中去定义路由，而是直接通过 layuiAdmin 的前端路由去访问，即可匹配相应目录的视图，从而呈现出页面结果。

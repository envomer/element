## 安装

### npm 安装
推荐使用 npm 的方式安装，它能更好地和 [webpack](https://webpack.js.org/) 打包工具配合使用。

```shell
npm i element-ui -S
```

### CDN
目前可以通过 [unpkg.com/element-ui](https://unpkg.com/element-ui/) 获取到最新版本的资源，在页面上引入 js 和 css 文件即可开始使用。

```html
<!-- 引入样式 -->
<link rel="stylesheet" href="https://unpkg.com/element-ui/lib/theme-default/index.css">
<!-- 引入组件库 -->
<script src="https://unpkg.com/element-ui/lib/index.js"></script>
```

### Hello world
通过 CDN 的方式我们可以很容易地使用 Element 写出一个 Hello world 页面。[在线演示](http://codepen.io/QingWei-Li/pen/vXwJrY)

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <!-- 引入样式 -->
  <link rel="stylesheet" href="https://unpkg.com/element-ui/lib/theme-default/index.css">
</head>
<body>
  <div id="app">
    <el-button @click="visible = true">按钮</el-button>
    <el-dialog v-model="visible" title="Hello world">
      <p>欢迎使用 Element</p>
    </el-dialog>
  </div>
</body>
  <!-- 先引入 Vue -->
  <script src="https://unpkg.com/vue/dist/vue.js"></script>
  <!-- 引入组件库 -->
  <script src="https://unpkg.com/element-ui/lib/index.js"></script>
  <script>
    new Vue({
      el: '#app',
      data: function() {
        return { visible: false }
      }
    })
  </script>
</html>
```
如果是通过 npm 安装，并希望配合 webpack 使用，请阅读下一节：快速上手。

#### Vue移动端适配方案

vue项目配置px2rem

- 首先，我们使用 vue 的脚手架 vue-cli 初始化一个 webpack 项目（前提是已经安装过 vue-cli，具体不再阐述），一些选项根据自己项目需要选择。

  `此处是vue-cli2的创建项目方式`

```
vue init webpack my-app     
```

- 命令执行之后，会在当前目录生成一个以“my-app”命名的项目文件夹。进入项目目录：

```
cd my-app
```

- 使用`yarn` 安装项目所需依赖后，安装 `lib-flexible` 和  `px2rem-loader`：

```
yarn add lib-flexible
yarn add px2rem-loader --dev
```

- 在入口页面 index.html 中设置``标签：

```
<meta name="viewport" content="width=device-width,inital-scale=1.0,
    maximum-scale=1.0,minimum-scale=1.0,user-scalable=no">
```

- 然后在项目入口文件 main.js 中引入 `lib-flexible`：

  ```
  import "lib-flexible/flexible.js" ;
  ```

- 在build文件夹下的utils.js添加

 

   

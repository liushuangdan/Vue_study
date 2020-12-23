## Vue 的安装

#### 1、 独立版本
 像js 一样，在Vue.js的官网上下载vue.min.js，并用`<script>`标签引入。

 #### 2、使用CDN的方法
1. Staticfile CDN（国内） : https://cdn.staticfile.org/vue/2.2.2/vue.min.js

2. unpkg：https://unpkg.com/vue/dist/vue.js, 会保持和 npm 发布的最新的版本一致。

3. cdnjs : https://cdnjs.cloudflare.com/ajax/libs/vue/2.1.8/vue.min.js

#### 3、NPM方法
由于npm安装速度慢，建议使用淘宝NPM镜像，下载速度快 cnpm 下载速度快

安装步骤：

    1. 从node.js的官网下载node.js  
    2. 安装node.js,基本上是一路next,重点是要选择安装的位置本次演示选择安装在E:\nodejs里
    3. 安装完毕后,配置node.js
       1. 安装完毕后,配置node.js

            运行cmd

            执行npm路径配置命令

            npm config set prefix "E:\nodejs\node_global"npm config set cache "E:\nodejs\node_cache"

            查看本地仓库

            npm list -global

            更换镜像站为国内的淘宝镜像站

            npm config set registry=http://registry.npm.taobao.org

            查看本地镜像能不能通

            npm config get registry

            注意，此时，默认的模块E:\nodejs\node_modules 目录将会改变为E:\nodejs\node_global\node_modules 目录，如果直接运行npm install等命令会报错的。增加环境变量NODE_PATH 内容是：E:\nodejs\node_global\node_modules

            关闭cmd
    4. 安装vue相关的包
        1. 重新打开cmd

            npm install vue -g 安装vue npm install vue-router -g 安装vue-router npm install vue-cli -g 安装vue脚手架这里的-g是指安装到global全局目录去

            安装完成后，此时安装的文件都会到E:\nodejs\node_global\node_modules中

        2. 关闭cmd

            对path环境变量添加E:\nodejs\node_global

        3. 重新打开cmd


运行vue -V ,如果显示版本号 则到此安装完成
    
---
以上方式用 npm 安装， 下载的速度慢，建议使用[Vue依赖](Vue依赖.md)中的安装方法


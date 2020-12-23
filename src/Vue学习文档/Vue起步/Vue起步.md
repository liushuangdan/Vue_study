初学者测试用例
===

下载Vue的js文件地址：https://cdn.staticfile.org/vue/2.4.2/vue.min.js

* 最基础版的，创建一个html文件，引入vue.js文件，在div中设置一个id

```
<div id="vue_det">
</div>
```
* 写js 来控制这个 容器

 Vue 构造器中有一个el 参数，它是 DOM 元素中的 id。在上面实例中 id 为 vue_det，在 div 元素中

```
<script type="text/javascript">
    var vm = new Vue({
        el: '#vue_det',
        data: {
            site: "刘丹丹同学",
            url: "www.nihao.com",
            alexa: "10000万"
        },
        methods: {
            details: function() {
                return  this.site + " - 胖的就剩骨头了！";
            }
        }
    })
</script>
```
这意味着我们接下来的改动全部在以上指定的 div 内，div 外部不受影响。

* 接下来我们看看如何定义数据对象。

data 用于定义属性，实例中有三个属性分别为：site、url、alexa。

methods 用于定义的函数，可以通过 return 来返回函数值。

{{ }} 用于输出对象属性和函数返回值

details()调用这个函数，输出返回值

```
<div id="vue_det">
    <h1>site : {{site}}</h1>
    <h1>url : {{url}}</h1>
    <h1>{{details()}}</h1>
</div>
```

* 当一个Vue实例被创建时，它向Vue的响应式系统中加入了其 data对象中能找到的所有的属性。 
* 当这些属性的值发生改变时，html视图将会产生相应的变化。
  
```
<script type="text/javascript">
// 我们的数据对象
var data = { site: "刘丹丹同学", url: "www.你好.com", alexa: '1万'}
var vm = new Vue({
    el: '#vue_det',
    data: data
})
// 它们引用相同的对象！
document.write(vm.site === data.site) // true
document.write("<br>")
// 设置属性也会影响到原始数据
vm.site = "双美"
document.write(data.site + "<br>") // 双美
 
// ……反之亦然
data.alexa = 1234
document.write(vm.alexa) // 1234
</script>

```

* 除了数据属性，Vue 实例还提供了一些有用的实例属性与方法。它们都有前缀 $，以便与用户定义的属性区分开来。例如：
  
```
<script type="text/javascript">
// 我们的数据对象
var data = { site: "Dandan", url: "www.nihao.com", alexa: '1w'}
var vm = new Vue({
    el: '#vue_det',
    data: data
})
 
document.write(vm.$data === data) // true
document.write("<br>") 
document.write(vm.$el === document.getElementById('vue_det')) // true
</script>

```


# vuerouter-small-project
通过开发一个后台管理系统，来学习vue-router的基本使用。

无需安装任何模块，可以直接运行。
暂时没有使用模块化开发，目的是为了体验vue-router最基本的功能。
![image](https://github.com/feixiangzhang/vuerouter-small-project/blob/master/images/page.png)

简要总结知识点：  
1、 通过添加<router-link to="/users">点我渲染页面</router-link> 来增加路由导航链接， router-link标签会被编译成 a 标签， to属性相当于 href属性，to属性的值是个相对地址，
对应后面要讲的路由地址，本质上是一个锚点。  
2、 通过添加<router-view></router-view> 在页面添加一个路由视图，本质上就是一个占位符，后面匹配到的组件会在这里渲染。  
3、 定义组件，就是各种各样的页面，可以用 简单的js对象{}来定义组件， 当然正常开发是要用单独的 .vue文件来定义单个组件。  
4、 实例化VueRouter,并在其构造函数中，定义参数对象的属性 routes ,这是一个数组，里面定义了路由的匹配规则，非常非常重要！！！  
5、 最后讲VueRouter实例，注入到Vue实例中，这样在任何子组件重都可以方便的使用vue-router    
6、 本案例重使用到了嵌套子路由，即在组件模板中使用了路由导航功能，那么要在该组件的路由规则中，添加children属性，在这里为子路由添加路由规则
7、 同时用到了路由动态参数和传参规则 ，即匹配路径用 冒号开头代表动态参数 如 /users/:id  这里id为动态参数，  
8、 最后一点 编程式导航，js代码中通过this.$router.push('') 可以直接在<router-view />中渲染想匹配的组件，它相当于router-link，只是不用添加然后html标签。  
this.$router.go(-1) / 1  用来返回上一页，或者前进下一页。 这里的前进后退都不会刷新网页，都是针对的路由导航。  
  
最后的组合，命名式router-link和 命名路由视图 我会在后面用到再介绍  

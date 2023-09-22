### 任务1
  主页显示文章列表，每篇文章可以被阅读，阅读后可以点赞，点赞数初始为0;
  并把代码上传到gitee或者github代码库进行管理。
  步骤过程及代码
  1.添加镜像 npm install -g cnpm --registry=http://registry.npm.taobao.org
  2.搭建VUE3项目
    npm create vue@latest
  3.安装Vscode插件：Volar，path
  4.整合vue-router+pinia+axios+element-plus
    cnpm i vue-router pinia axios element-plus
    cnpm install -D unplugin-vue-components unplugin-auto-import
  5.在src目录里搭建/router/index.js
    //route 访问路径，路由
    //router 路由管理者
    import { createRouter, createWebHashHistory } from 'vue-router';
    // 创建路由实例并传递 `routes` 配置const router = createRouter({// 内部提供了 history 模式的实现。为了简单起见，我们在里使用 hash 模式。
    //创建路由 route
    import Home  from  "@/views/Home.vue"
    import About  from  "@/views/About.vue"
    const routes = [
      { path: '/', component: Home },
      { path: '/about', component: About },
    ]
    //创建路由管理 router
    const router = createRouter({// 内部提供了 history 模式的实现。为了简单起见，我们在这里使用 hash 模式。
       history: createWebHashHistory(),
      routes,}
     );
    //导出路由
    export default router
    5.1挂载main.js
    // 创建实例
      import router from './router'
      const app = createApp(App);//确保 _use_ 路由实例使整个应用支持路由。
      app.use(router);// 挂载router,完成
      app.mount('#app');
    5.3路由简单使用App.vue
    <template>
      <RouterLink to="/">首页</RouterLink>
      <RouterLink to="/about">用户中心</RouterLink>
      <div>
      <!-- 页面组件的占位 iframe -->
      <RouterView></RouterView> 
      </div>
   </template>
   5.4 编写Home.vue文件实现文章点赞
    <template>
        <div>Home</div>
        <div>{{ msg }}</div>
        <div v-html="rawHtml"></div>
        <img src="./tu1.jpeg" height="100" width="100" alt="">
        <span>点赞{{count}}</span>
        <button v-on:click="btnCount">点赞</button>
    </template>
    <script>
    //
    export default{
        setup(){

        },data(){
            return{
                msg:"hello vue",
                rawHtml:"学而不思则罔。一《论语》",
                src:'',
                count:0
            }
        },methods:{
            //
            btnCount(){
                this.count++
            }
        }
    }
    </script>
  6.创建github代码库名称"vue-router+pinia+axios+element-plus"上传
    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin https://github.com/cfb-111/vue-router-pinia-axios-element-plus.git
    git push -u origin main

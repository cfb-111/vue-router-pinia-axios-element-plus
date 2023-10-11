###练习弹性盒子布局
步骤过程及代码
1.创建文件Login.vue
2.在index.js添加文件路径
    import Login  from  "@/views/Login.vue"
    const routes = [
        { path: '/login', component: Login },
    ]
3.在Login.vue编写弹性盒子布局代码
    <script></script>
    <template>
        <div class="login">Login
            <div class="inner">1</div>
            <div class="inner">2</div>
            <div class="inner">3</div>
            <div class="inner">4</div>
        </div>
    </template>
    <style>
    .login.flex-container{
        /*容器*/
        display: flex;
        list-style: none;
        margin: 0;
        padding: 0;
        flex-direction: column;/*垂直排序*/
        /*justify-content: center;/*水平居中
        align-items:center;/*垂直居中*/
    }

    .inner{
        width: 200px;
        height: 200px;
        border: 1px solid #ccc;
        background-color: darkseagreen;
    }
    </style>
4.创建github代码库名称"vue-router+pinia+axios+element-plus"上传
    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin https://github.com/cfb-111/vue-router-pinia-axios-element-plus.git
    git push -u origin main

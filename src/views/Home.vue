
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

<template>
  <div class="recommendview">
<div v-for=" item in recommends" :key="item.background" class="recommend-item">
    <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{item.title}}</div>
    </a>
</div>
  </div>
</template>

<script>
export default {
name:"RecommendView",
props:{
    recommends:{
        type:Array,
    default(){
        return[]
    }
}
    }
}
</script>

<style>
.recommendview{
    display: flex;
    width: 100%;
    text-align: center;
}
.recommend-item{
    flex: 1;
}
.recommendview img{
    width: 80px;
    height: 80px;
    margin-bottom: 5px;
   
}
</style>
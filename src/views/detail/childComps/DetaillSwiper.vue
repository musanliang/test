<template>
  <div class="detail-swiper">
    <swiper class="swiper1">
       <swiper-item v-for=" item in topImages" :key='item'> 
           <img :src="item" alt="">
       </swiper-item>
   </swiper>
  </div>
  
</template>
  
<script>
import {Swiper, SwiperItem} from 'components/common/swiper';
export default {
 name:'DetaillSwiper',
 components:{
    Swiper,
    SwiperItem
 },
 props:{
      topImages:{
          type:Array,
          default(){
              return[]
          }
      }
 }
}
</script>

<style scope>
 .swiper1{
     height: 300px;
     overflow: hidden;
 }
</style>
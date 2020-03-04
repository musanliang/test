<template>
  <div class="tab-control">
      <div v-for="(item,index) in titles" :key="item.background" 
      class="tab-control-item" :class="{active : index === currentindex}" @click="itemClick(index)">
          <span>{{item}}</span>
      </div>
  </div>
</template>

<script>
export default {
name:"TabControl",
props: {
    titles:{
        type:Array,
        deafult(){
            return []
        }
    }
},
data () {
    return {
        currentindex : 0
    }
},
methods: {
    itemClick(index){
        this.currentindex = index;
        this.$emit('tabClick', index)
    }
}
}
</script>

<style>
.tab-control{
    display: flex;
    text-align: center;
}
.tab-control-item{
    flex: 1;
    height: 44px;
    line-height: 44px;
   padding-bottom: 3px;
}
.active{
    color: var(--color-high-text);
    
}
.active span{
    border-bottom:  2px solid var(--color-high-text);
}
</style>
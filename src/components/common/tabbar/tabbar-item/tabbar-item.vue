<template>

  <div @click="itemClick" class="tab-bar-item">

    <slot v-if="!isActive" name="item-icon"></slot>
    <slot v-else name="item-icon-active"></slot>


    <div :style="activeStyle"><slot name="item-text"></slot></div>
  </div>

</template>

<script>
  export default {
    name: "tabbaritem",
    data(){
      return {

      }
    },
    computed:{
      isActive(){
        return this.$route.path.indexOf(this.path) !== -1;
      },
      activeStyle(){
        return this.isActive?{color:this.activeColor}:{};
      }
    },
    props:{
      path:String,
      activeColor:{
        type:String,
        default:"red",
      }
    },
    methods:{
      itemClick(){

        this.$router.replace(this.path);
      }
    }
  }
</script>

<style scoped>


  .tab-bar-item {
    flex:1;
    text-align: center;
    height:49px;
    font-size: 14px;
  }
  .tab-bar-item img{
    height: 24px;
    width: 24px;
    margin-top:3px;
  }


</style>

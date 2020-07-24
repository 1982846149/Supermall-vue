<template>
  <div>
  <tabbar>
    <tabbaritem path="/home" >
      <img src="../../../assets/img/tabbar/home.svg" slot="item-icon">
      <img src="../../../assets/img/tabbar/home_active.svg" slot="item-icon-active">
      <div slot="item-text">首页</div>
    </tabbaritem>



    <tabbaritem path="/category" >
      <img src="../../../assets/img/tabbar/category.svg" slot="item-icon">
      <img src="../../../assets/img/tabbar/category_active.svg" slot="item-icon-active">
      <div slot="item-text">分类</div>
    </tabbaritem>

    <tabbaritem path="/cart" >
      <img src="../../../assets/img/tabbar/shopcart.svg" slot="item-icon">
      <img src="../../../assets/img/tabbar/shopcart_active.svg" slot="item-icon-active">

      <div slot="item-text">购物车</div>
    </tabbaritem>

    <tabbaritem path="/profile" >
      <img src="../../../assets/img/tabbar/profile.svg" slot="item-icon">
      <img src="../../../assets/img/tabbar/profile_active.svg" slot="item-icon-active">

      <div slot="item-text">我的</div>
    </tabbaritem>


  </tabbar>
  </div>
</template>

<script>
  import tabbar from "../../../components/common/tabbar/tabbar/tabbar";
  import tabbaritem from "../../../components/common/tabbar/tabbar-item/tabbar-item"
  export default {
    name: "maintabbar",
    components:{
      tabbar,
      tabbaritem,
    }
  }
</script>

<style scoped>

</style>

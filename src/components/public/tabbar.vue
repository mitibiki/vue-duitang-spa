<template>
<div>
<mt-tabbar v-model="selected" fixed>


  <mt-tab-item id="首页">
    <router-link to="/firstpage">
    <icon name="home" v-if="selected==='首页'" color="#FE5858"></icon>
    <icon name="home" v-if="selected != '首页'"></icon><br>
    首页  </router-link>
  </mt-tab-item>



  <mt-tab-item id="发现">
    <router-link to="/discovery">
    <icon name="compass" v-if="selected==='发现'" color="#FE5858"></icon>
    <icon name="compass" v-if="selected !='发现'"></icon><br>
    发现 </router-link>
  </mt-tab-item>


  <mt-tab-item id="商店">
  <router-link to="/shop">
    <icon name="shopping-basket" v-if="selected==='商店'" color="#FE5858"></icon>
    <icon name="shopping-basket" v-if="selected !='商店'"></icon><br>
    商店 </router-link>
  </mt-tab-item>



  <mt-tab-item id="我的">
    <router-link to="/mine">
    <icon name="user" v-if="selected==='我的'" color="#FE5858"></icon>
    <icon name="user" v-if="selected !='我的'"></icon><br>
    我的 </router-link>
  </mt-tab-item>


</mt-tabbar>



</div>
</template>
<script>
export default {
data () {
      return {
        selected: '首页'
      }
    }
}
</script>
<style lang="stylus" scoped>
.mint-tab-item-label a
  display inline-block
  width 100%
  height 100%
</style>

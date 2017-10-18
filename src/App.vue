<template>
  <div id="app">    
    <nav class="navigation">
      <router-link tag="a" 
                   v-for="(item, index) in menu" 
                   :key="index" 
                   :to="item.path" 
                   class="nav-item" 
                   active-class="nav-item-active" exact> {{ index + 1 }}. {{ item.name }} </router-link>
    </nav>
    <div class="examples">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import { routes } from './router'

export default {  
  data () {
    return {
      menu: routes
    }
  }
}
</script>

<style lang="stylus" scoped>
.navigation
  height 100%
  width 12%
  display inline-block 
  vertical-align top
  padding 10px 10px 10px 10px

  .nav-item
    display block
    text-decoration none
    margin-top 5px
    color green
    transition 500ms

    &:hover
      color blue
  
  .nav-item-active
    color blue

.examples
  background-color #EAEAEA
  padding 10px 10px 10px 10px
  height 100%
  width 84%
  display inline-block
  vertical-align top
  position absolute
</style>

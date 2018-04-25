<template>
  <div id="app">
    <ul class="nav">
      <li v-for="(item,index) in nav">
         <router-link :to="item.url">{{ item.name }}</router-link>
      </li>
    </ul>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      nav:[
        {name:"导航1",url:"/"},
        {name:"导航2",url:"/navTwo"}
      ]
    }
  }
}
</script>

<style>
.nav {display:inline-block;}
.nav li {float:left;list-style:none;}
</style>

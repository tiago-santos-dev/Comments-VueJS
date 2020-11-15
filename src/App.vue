<template>
  <div id="app">
    <b-tabs>
   <b-tab title="Comments" active>
      <list/>
   </b-tab>
   <b-tab title="Add New">
      <register/>
   </b-tab>

</b-tabs>
  </div>
</template>

<script>
import list from './components/list'
import register from './components/register'
export default {
  name: 'App',
  components:{
    list,
    register   
  }
}
</script>

<style>

</style>

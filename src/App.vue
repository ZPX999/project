<template>
  <div>
    <h1 class="topic">后台管理系统</h1>
    <div class="">
      <RequestList/>
    </div>
    
  </div>
</template>

<script>

import RequestList from './components/RequestList.vue';
export default {
  name: 'App',
  components: {
    RequestList,
  },
}
</script>

<style>
  .topic {
    position: relative;
    left: 40%;
  }
</style>

<template>
  <div class="styleLists">
    <div>
      <OneList :cubes="cubes" />
    </div>
  </div>
</template>

<script>
import OneList from './OneList.vue';

  export default {
    props :{
      cubes:{
      type: Array
    }
  },
    components : {
      OneList
    }
  }
</script>

<style scoped>
.styleLists {
  border: 2px solid rgb(10, 155, 0);
  padding: 15px;
}
</style>
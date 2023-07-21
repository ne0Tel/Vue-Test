<template>

  <div class="_container styleApp">
    <MoreLists class="_flex-col" :cubes="cubes"/>
    <ViewCostum class="_flex-col" :cubes="cubes"/>
  </div>
  
</template>

<script>
import MoreLists from './Components/MoreLists.vue';
import ViewCostum from './Components/ViewCostum.vue';

  export default {
    components: {
    MoreLists,
    ViewCostum
  },
    data() {
      return {
        cubes: [
          {id: 1, count: 10, color: "#ff0000", checked: false},
          {id: 2, count: 16, color: "#fff700", checked: false},
          {id: 3, count: 40, color: "#33ff00", checked: false},
          {id: 4, count: 0, color: "#0055ff", checked: false},
      ],
      }
    },
    methods: {

    }
  }
</script>

<style>
/*----------------Reboot Start----------------*/
*,
*::before,
*::after {
  padding: 0px 0px 0px 0px;
  margin: 0;
  border: 0;
  box-sizing: border-box;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-weight: inherit;
  font-size: inherit;
}

a {
  text-decoration: none;
}

img {
  vertical-align: top;
}

ul,
ol,
li {
  list-style: none;
}

html,
body {
  background: #fafafa;
  height: 100%;
  line-height: 1;
  font-family: Montserrat;
  font-size: 20px;
  font-weight: 500;
  color: #252b42;
}

.wrapper {
  min-height: 100%;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}

._container {
  max-width: 1046px;
  margin: 0px auto;
  padding: 0 15px;
  box-sizing: content-box;

  display: flex;
}

._flex-col {
  flex: 0 1 50%;
  text-align: center;
}

/*----------------Reboot End----------------*/

.styleApp {
  border: 1px solid rgb(10, 155, 0);
  padding: 15px;
  margin-top: 15px;
}
</style>
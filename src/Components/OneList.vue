<template>

  <!-- Первый список Item -->
  <div class="_flex">
    <a href="#" @click="toggleElement">
      <img src="@/Img/free-icon-arrow-point-to-right-32213.png" alt="">
    </a>
    <input type="checkbox">
    <label for="">List 1</label>
  </div>

  <!-- Отрисовка Item через цикл и накидывание v-model на каждый компонент -->
  <div v-show="isVisible">
    <OneItem
    v-for="item in cubes"
    v-bind:key="item.id"
    :item="item"
    v-model:check="item.checked"
    />
  </div>
</template>

<script>
import OneItem from "@/Components/OneItem.vue";

  export default {
    data() {
    return {
      isVisible: false,
    }
  },
    props: {
      cubes: {
        type: Array
      }
    },
    components : {
      OneItem
    },
    methods: {
      toggleElement() {
      this.isVisible = !this.isVisible;
    }
    }
  }
</script>

<style scoped>
._flex {
  display: flex;
  align-items: center;
}

._flex > *:not(:last-child) {
  margin: 0px 5px 0px 0px;
}

img {
  width: 15px;
  height: 15px;
}

</style>
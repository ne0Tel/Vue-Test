<template>
  <div class="_flex-col">

    <!-- Checkbox и номер Item -->
    <div class="_flex">
      <input :checked='check' @change="updateInput" type="checkbox">
      <label for="">Item {{ item.id }}</label>
    </div>
    
    <!-- Количество и цвет квадратов -->
    <div class="_flex">
      <label for="">{{ item.count }}</label>
      <div v-bind:style="{ backgroundColor: item.color, width: '15px', height: '15px' }"></div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      item: {
        type: Object
      },
      check: {
        type: Boolean
      }
    },
    methods : {
      updateInput(event) {
        this.$emit('update:check', event.target.checked)
      }
    }
  }
</script>

<style scoped>
._flex {
  display: flex;
}
._flex > *:not(:last-child) {
  margin: 0px 5px 0px 45px;
}

._flex-col{
  display: flex;
  justify-content: space-between;
}
</style>
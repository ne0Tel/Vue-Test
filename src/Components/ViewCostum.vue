<template>
  <div class="styleView">
    <div class="listNum">

      <!-- Заголовок и кнопка -->
      <div class="_flex-row">
        <label for="">List 1</label>
        <button class="btn">Отсоритировать</button>
      </div>
  
      <!-- Отрисовка квадратов если item.checked === true  -->
      <div class="_flex" v-for="item in cubes" v-bind:key="item.id">
        
        <div class="_flex" v-if="item.checked">
          <div v-for="i in item.count" v-bind:key="i.id">
            <div v-bind:style="{ backgroundColor: item.color, width: '15px', height: '15px', margin: '0px 2px 2px 0px'}"></div>
          </div>
        </div>   
      </div>

    </div>
  </div>
</template>

<script>
  export default {
    props: {
      cubes: {
        type: Array
      } 
    }
  }
</script>

<style scoped>
._flex{
  display: flex;
  flex-wrap: wrap;
}
._flex-row {
  display: flex;
  justify-content: space-between;
}

.listNum {
  border: 2px solid #0a9b00;
  padding: 15px;
}

.styleView {
  border: 2px solid #0a9b00;
  padding: 15px;
}

.styleView > *:not(:last-child) {
  margin: 0px 0px 10px 0px;
}

.btn {
  padding: 5px;
  background-color: #0352e3;
  color: aliceblue;
  border-radius: 10px;
}
</style>
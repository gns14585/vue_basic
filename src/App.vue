<template>
  <div>
    <!--    <div v-if="isVisible" class="red"></div>-->
    <!--    <div v-if="isVisible === true" class="blue"></div>-->
    <!--    <div v-else class="black"></div>-->
    <div v-if="count > 1" class="red"></div>
    <div v-else class="blue"></div>

    <button @click="count++">증가</button>
    <button @click="count--">감소</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: true,
      count: 0,
    };
  },
};
</script>

<style scoped>
.red {
  width: 100px;
  height: 100px;
  background-color: red;
}
.blue {
  width: 100px;
  height: 100px;
  background-color: blue;
}
.black {
  width: 100px;
  height: 100px;
  background-color: black;
}
</style>

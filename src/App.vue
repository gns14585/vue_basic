<template>
  <button @click="changeMessage">{{ message }}</button>
  {{ watchMessage }}
</template>

<script>
export default {
  data() {
    return {
      message: "안녕하세요, Vue.js Watch 기능 테스트 오리지널 문구",
      watchMessage: "",
    };
  },
  watch: {
    message() {
      // window.alert("message 변수에 담긴 데이터가 변경되었습니다.");
      this.watchMessage = "Watch 동작";
    },
  },
  methods: {
    changeMessage() {
      console.log("함수 호출");
      this.message = "변경된 message 데이터 입니다.";
    },
  },
};
</script>

<style lang="scss" scoped></style>

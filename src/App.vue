<template>
  <div>
    <ChildComponent
      :sendProps1="title"
      :sendProps2="createAt"
      :sendProps3="obj"
    />
  </div>
</template>

<script setup lang="ts">
import ChildComponent from "@/components/ChildComponent.vue";
import { reactive, ref } from "vue";

interface Obj {
  id: number;
  name: string;
}

const title = ref<string>("부모 컴포넌트에서 선언된 데이터 입니다.");
const createAt = ref<number>(2024);
const obj = reactive<Obj>({
  id: 2024,
  name: "John",
});
</script>

<style lang="scss" scoped></style>

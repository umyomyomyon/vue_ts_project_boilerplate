<template>
  <div>
    <p>これはテストコンポーネント</p>
    <p class="text">props.text(色は赤になるはず): {{ text }}</p>
    <ul>
      <p>配列を表示</p>
      <li v-for="(item, index) in numberList" :key="index">
        {{ item }}
      </li>
    </ul>
    <div>{{ obj.key1 }}</div>
    <div>{{ obj.key2 }}</div>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from "@vue/composition-api";

type objType = { key1: string; key2: number };

type Props = {
  text: string;
  numberList: number[];
  obj: objType;
};

export default defineComponent({
  props: {
    text: {
      type: String,
      required: true
    },
    numberList: {
      type: Array as PropType<number[]>,
      required: false,
      default: () => [10, 9, 8, 7, 6, 5]
    },
    obj: {
      type: Object as PropType<objType>,
      required: false,
      default: () => ({ key1: "default", key2: 0 })
    }
  },
  setup(props: Props) {
    const text = props.text; //string
    const numberList = props.numberList; //number[]
    const obj = props.obj; //objType
  }
});
</script>

<style scoped lang="scss">
.text {
  color: red;
}
</style>

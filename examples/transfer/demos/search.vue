<template>
  <div>
    <t-transfer v-model="targetValue" theme="primary" :data="list" :checked-value="checkedValue" :search="true" />
  </div>
</template>
<script>
import { defineComponent, ref } from 'vue';

const list = [];
for (let i = 0; i < 20; i++) {
  list.push({
    value: i.toString(),
    label: `内容${i + 1}`,
  });
}

export default defineComponent({
  setup() {
    const targetValue = ref([]);
    const checkedValue = ref([]);
    return {
      checkedValue,
      targetValue,
      list,
    };
  },
});
</script>

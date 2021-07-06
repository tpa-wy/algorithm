<template>
  <div>
    <h2>D&C快速排序</h2>
    <!-- 计算数组的和 -->
    <div>list数组：{{ list }} 的和为{{ this.sum(list) }}</div>
  </div>
</template>

<script>
export default {
  name: "MyProjectFastsort",

  data() {
    return {
      list: [10, 20, 30],
    };
  },

  mounted() {
  },

  methods: {
    sum(list) {
      let _list = [...list];
      if (list.length === 0) {
        return 0;
      }
      _list.splice(0, 1);
      // 解析为 10 + sum([20,30])
      // 解析为 10 + 20 + sum([30])
      // 解析为 60
      return list[0] + this.sum(_list);
    },
  },
};
</script>

<style lang="scss" scoped></style>

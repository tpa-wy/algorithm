<template>
  <div>
    <h2>快速排序（从小到大）---- 选择排序的升级版</h2>
    <!-- 排序list -->
    <div>需要排序的数组：{{ arr }}</div>
    <div>排序完成的数组：{{ this.quicksort(arr) }}</div>
  </div>
</template>

<script>
export default {
  name: "MyProjectFastsortnumber",

  data() {
    return {
      arr: [5, 3, 6, 2, 10, 9, 9],
    };
  },

  mounted() {},

  methods: {
    quicksort(list) {
      if (list.length < 2) {
        return list;
      }
      let _list = [...list];
      // 选择基准值
      let pivot = _list[0];
      _list.splice(0, 1);
      let less = _list.filter((item) => item <= pivot);
      let greater = _list.filter((item) => item > pivot);
      return [...this.quicksort(less), pivot, ...this.quicksort(greater)];
    },
  },
};
</script>

<style lang="scss" scoped></style>

<template>
  <div>
    <h2>选择排序</h2>
    <div>需要排序的数组：{{ arr }}</div>
    <div>排序完成的数组：{{ this.init() }}</div>
  </div>
</template>

<script>
export default {
  name: "MyProjectSelectionsort",
  data() {
    return {
      arr: [5, 3, 6, 2, 10, 9, 9],
    };
  },

  mounted() {},

  methods: {
    init() {
      this.sort(this.arr);
      console.time("选择排序执行时间");
      let list = this.sort(this.arr);
      console.timeEnd("选择排序执行时间");
      return list;
    },
    getsmallArr(arr) {
      let smallest = arr[0];
      let smallest_index = 0;
      for (var i in arr) {
        if (arr[i] < smallest) {
          smallest = arr[i];
          smallest_index = i;
        }
      }
      return smallest_index;
    },
    sort(arr) {
      let _arr = [...arr];
      let list = [];
      for (var i in arr) {
        let smallest_index = this.getsmallArr(_arr);
        list.push(_arr[smallest_index]);
        _arr.splice(smallest_index, 1);
      }
      return list;
    },
  },
};
</script>

<style lang="scss" scoped></style>

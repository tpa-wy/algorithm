<template>
  <div>
    <h2>选择排序</h2>
    <div>需要排序的数组：{{ arr }}</div>
    <div v-show="arr2">排序完成的数组：{{ arr2 }}</div>
  </div>
</template>

<script>
export default {
  name: "MyProjectSelectionsort",
  data() {
    return {
      arr: [5, 3, 6, 2, 10,9],
      arr2: [],
    };
  },

  mounted() {
    this.sort(this.arr);
  },

  methods: {
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
    sort(arr){
        let _arr = [...arr]
        for(var i in arr){
            let smallest_index = this.getsmallArr(_arr)
            this.arr2.push(_arr[smallest_index])
            _arr.splice(smallest_index,1)
        }
    }
  },
};
</script>

<style lang="scss" scoped></style>

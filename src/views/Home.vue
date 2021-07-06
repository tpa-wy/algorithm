<template>
  <div>
    <!-- 二分查找 -->
    <BinarySearch />
    <!-- 选择排序 -->
    <SelectionSort />
    <!-- 递归 -->
    <Recursive />
  </div>
</template>

<script>
import BinarySearch from "../components/BinarySearch.vue";
import Recursive from "../components/Recursive.vue";
import SelectionSort from "../components/SelectionSort.vue";
export default {
  name: "MyProjectHome",
  components: { BinarySearch, SelectionSort, Recursive },
};
</script>

<style lang="scss" scoped></style>

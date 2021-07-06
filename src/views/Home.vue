<template>
  <div>
    <!-- 二分查找 -->
    <BinarySearch />
    <!-- 选择排序 -->
    <SelectionSort />
    <!-- 递归 -->
    <Recursive />
    <!-- 递归调用栈 -->
    <StackRecursive />
    <!-- 快速排序 -->
    <FastSort />
    <!-- 快速排序（从小到大） -->
    <FastSortNumber />
    <!-- 递归节点树 -->
    <RecursiveTree />
  </div>
</template>

<script>
import BinarySearch from "../components/BinarySearch.vue";
import FastSort from "../components/FastSort.vue";
import Recursive from "../components/Recursive.vue";
import SelectionSort from "../components/SelectionSort.vue";
import StackRecursive from "../components/StackRecursive.vue";
import FastSortNumber from "../components/FastSortNumber.vue";
import RecursiveTree from "../components/RecursiveTree.vue";
export default {
  name: "MyProjectHome",
  components: {
    BinarySearch,
    SelectionSort,
    Recursive,
    StackRecursive,
    FastSort,
    FastSortNumber,
    RecursiveTree,
  },
};
</script>

<style lang="scss" scoped></style>

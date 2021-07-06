<template>
  <div>
    <h2>递归调用栈</h2>
    <!-- 计算阶乘 -->
    <div>5 的阶乘={{ this.init() }}</div>
  </div>
</template>

<script>
export default {
  name: "MyProjectStackrecursive",

  data() {
    return {};
  },

  mounted() {},

  methods: {
    init() {
      console.time("递归调用栈执行时间");
      let list = this.factorial(5);
      console.timeEnd("递归调用栈执行时间");
      return list;
    },
    factorial(factorial) {
      if (factorial === 1) {
        return 1;
      } else {
        return factorial * this.factorial(factorial - 1);
      }
    },
  },
};
</script>

<style lang="scss" scoped></style>

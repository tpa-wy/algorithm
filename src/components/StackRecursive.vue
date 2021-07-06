<template>
  <div>
    <h2>递归调用栈</h2>
    <!-- 计算阶乘 -->
    <div>5 的阶乘={{ this.factorial(5) }}</div>
  </div>
</template>

<script>
export default {
  name: "MyProjectStackrecursive",

  data() {
    return {};
  },

  mounted() {
  },

  methods: {
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

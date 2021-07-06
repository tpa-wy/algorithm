<template>
  <div>
    <h2>递归</h2>
    <!-- 倒计时到 1 停止 -->
  </div>
</template>

<script>
export default {
  name: "MyProjectRecursive",
  data() {
    return {
      // 倒计时开始的数
      start: 3,
    };
  },

  mounted() {
    this.recursive(this.start);
  },

  methods: {
    // 递归函数
    recursive(startNumber) {
      console.log(startNumber);
      if (startNumber < 1) {
        return;
      }
      startNumber--;
      this.recursive(startNumber);
    },
  },
};
</script>

<style lang="scss" scoped></style>

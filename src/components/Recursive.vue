<template>
  <div>
    <h2>递归</h2>
    <!-- 倒计时到 1 停止 -->
    <div v-for="(item, index) in list" :key="index">{{ item }}</div>
  </div>
</template>

<script>
export default {
  name: "MyProjectRecursive",
  data() {
    return {
      // 倒计时开始的数
      start: 3,
      list: [],
    };
  },

  mounted() {
    this.init()
  },

  methods: {
    init() {
      this.recursive(this.start);
    },
    // 递归函数
    recursive(startNumber) {
      // console.log(startNumber);
      this.list.push(startNumber);
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

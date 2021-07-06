<template>
  <div>
    <h2>二分查找</h2>
    <div>现在在1 - 100 之间想一个整数数</div>
    <!-- <div>最小：{{min}},最大：{{max}}</div> -->
    <div @click="is_start = true" v-show="!is_start">开始</div>
    <div v-show="is_start">
      <div>是 {{ guessNumber }} 吗</div>
      <div>次数：{{ count }}</div>
      <div>
        <button @click="guess('big')">大了</button>
        <button @click="guess('smail')">小了</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MyProjectBinarysearch",
  data() {
    return {
      min: 1,
      max: 100,
      is_start: false,
      proportion: null,
      count: 0,
    };
  },

  mounted() {},
  computed: {
    guessNumber() {
      return Math.ceil((this.max + this.min) / 2);
    },
  },
  methods: {
    // 用户点击了大了或者小了
    guess(proportion) {
      this.count++;
      // 大了
      if (proportion === "big") {
        console.log("大了");
        this.proportion = "big";
        this.max = this.guessNumber - 1;
      } else {
        // 小了
        console.log("小了");
        this.min = this.guessNumber + 1;
        this.proportion = "smail";
      }
    },
  },
};
</script>

<style lang="scss" scoped></style>

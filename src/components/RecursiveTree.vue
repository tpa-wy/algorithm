<template>
  <div>
    <h2>递归节点树</h2>
    <!-- 递归节点树（根据pid） -->
    <div>处理节点树之前：{{ list }}</div>
    <div>处理节点树之后：{{ this.init() }}</div>
  </div>
</template>

<script>
export default {
  name: "MyProjectRecursivetree",

  data() {
    return {
      list: [
        { id: 1, name: "有限公司", pid: 0 },
        { id: 2, name: "键管部", pid: 1 },
        { id: 3, name: "技术部", pid: 1 },
        { id: 15, name: "技术一部", pid: 3 },
        // { id: 16, name: "技术一部一组", pid: 15 },
      ],
    };
  },

  mounted() {
  },
  methods: {
    init() {
      console.time("递归节点树执行时间");
      let tree = this.recursive(this.list);
      console.timeEnd("递归节点树执行时间");
      return tree;
    },
    recursive(list, pid = 0) {
      let tree = [];
      let temp;
      for (let i = 0; i < list.length; i++) {
        if (list[i].pid == pid) {
          let obj = list[i];
          temp = this.recursive(list, list[i].id);
        //   obj.label = list[i].name;
          if (temp.length > 0) {
            obj.children = temp;
          }
          tree.push(obj);
        }
      }
      return tree;
    },
  },
};
</script>

<style lang="scss" scoped></style>

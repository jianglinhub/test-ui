<template>
  <el-button type="primary" icon="el-icon-view" @click="toPage">审核</el-button>
</template>

<script>
export default {
  name: 'audit',
  props: {
    options: {
      type: Object,
      default() {},
      required: true,
    },
  },
  methods: {
    toPage() {
      this.$router.push({
        name: this.options.router,
        params: this.options.params,
        query: this.options.query,
      });
    },
  },
};
</script>

<template>
  <div class="demo-container">
    <h2>{{ title }}</h2>
    <p>{{ description }}</p>
    <!--显示代码区域-->
    <code-per :component="component"></code-per>
  </div>
</template>

<script lang="ts">
import CodePer from './CodePer.vue';

export default {
  name: 'demo-doc',
  components: {CodePer},
  props: {
    title: {
      type: String,
      default: '组件功能'
    },
    description: {
      type: String,
      default: '组件功能描述'
    },
    component: {
      type: Object
    }
  }
}
</script>

<style lang="scss" scoped>
.demo-container {
  h2 {
    font-weight: 400;
    color: #1f2f3d;
    font-size: 22px;
    margin: 55px 0 20px;
  }

  p {
    font-size: 15px;
    color: #5e6d82;
    line-height: 1.5em;
    margin: 14px 0;
  }
}
</style>
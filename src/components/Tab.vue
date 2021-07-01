<!--
 * @Author: hhhhhq
 * @Date: 2021-07-01 09:36:01
 * @LastEditors: hhhhhq
 * @LastEditTime: 2021-07-01 10:07:58
 * @Description: file content
-->
<template>
  <div class="tab-content" v-show="title == selectedTitle">
    <slot />
  </div>
</template>

<script>
import { inject } from "vue"

export default {
  props: ["title"],
  setup() {
    const selectedTitle = inject("selectedTitle")

    return {
      selectedTitle,
    }
  },
}
</script>

<style scoped>
.tab-content {
  min-height: 400px;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 3px 5px 5px rgba(0, 0, 0, 0.05);
}
</style>

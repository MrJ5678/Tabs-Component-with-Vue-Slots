<!--
 * @Author: hhhhhq
 * @Date: 2021-07-01 09:36:01
 * @LastEditors: hhhhhq
 * @LastEditTime: 2021-07-01 10:06:38
 * @Description: file content
-->
<template>
  <div class="tabs">
    <ul class="tabs__header">
      <li
        v-for="title in tabTitles"
        :key="title"
        :class="{ selected: title == selectedTitle }"
        @click="selectedTitle = title"
      >
        {{ title }}
      </li>
    </ul>
    <slot />
  </div>
</template>

<script>
import { ref, provide } from "vue"

export default {
  setup(props, { slots }) {
    const tabTitles = ref(slots.default().map(tab => tab.props.title))
    const selectedTitle = ref(tabTitles.value[0])

    provide("selectedTitle", selectedTitle)

    return {
      tabTitles,
      selectedTitle,
    }
  },
}
</script>

<style scoped>
.tabs {
  max-width: 400px;
  margin: 0 auto;
}

.tabs__header {
  margin-bottom: 10px;
  list-style: none;
  padding: 0;
  display: flex;
}

.tabs__header li {
  width: 80px;
  text-align: center;
  padding: 10px 20px;
  margin-right: 10px;
  background-color: #ddd;
  border-radius: 5px;
  transition: 0.4s all ease-out;
  cursor: pointer;
}

.tabs__header li.selected {
  background-color: #0984e3;
  color: white;
}
</style>

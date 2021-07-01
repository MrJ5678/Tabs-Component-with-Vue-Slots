<!--
 * @Author: hhhhhq
 * @Date: 2021-07-01 09:34:16
 * @LastEditors: hhhhhq
 * @LastEditTime: 2021-07-01 09:42:18
 * @Description: file content
-->
<template>
  <TabsWrapper>
    <Tab title="Tab1">Hello from Tab1</Tab>
    <Tab title="Tab2">Hello from Tab2</Tab>
    <Tab title="Tab3">Hello from Tab3</Tab>
    <Tab title="Tab4">Hello from Tab4</Tab>
  </TabsWrapper>
</template>

<script setup>
import TabsWrapper from "./components/TabsWrapper.vue"
import Tab from "./components/Tab.vue"
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

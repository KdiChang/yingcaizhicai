<template>
    <!-- <header>
    <img alt="Vue logo" class="logo" src="./assets/Logo.jpg" width="46.13" height="40" />
    <p class="title">映彩智材</p>
    <el-menu
      mode="horizontal"
      :ellipsis=false
    >
      <el-menu-item>实时</el-menu-item>
      <el-menu-item>规划</el-menu-item>
      <el-menu-item>规划</el-menu-item>
      <el-menu-item>管理员</el-menu-item>
    </el-menu>
    
  </header> -->
    <el-menu
      :default-active="activeIndex"
      class="el-menu-demo"
      mode="horizontal"
      :ellipsis="false"
      @select="handleSelect"
    >
      <el-menu-item index="0">
        <img src="../assets/Logo.jpg" width="100px"/>
      </el-menu-item>
      <div class="flex-grow" />
      <el-menu-item index="1">Processing Center</el-menu-item>
      <el-sub-menu index="2">
        <template #title>Workspace</template>
        <el-menu-item index="2-1">item one</el-menu-item>
        <el-menu-item index="2-2">item two</el-menu-item>
        <el-menu-item index="2-3">item three</el-menu-item>
        <el-sub-menu index="2-4">
          <template #title>item four</template>
          <el-menu-item index="2-4-1">item one</el-menu-item>
          <el-menu-item index="2-4-2">item two</el-menu-item>
          <el-menu-item index="2-4-3">item three</el-menu-item>
        </el-sub-menu>
      </el-sub-menu>
    </el-menu>
  </template>
  
  <script lang="ts" setup>
  import { ref } from 'vue'
  
  const activeIndex = ref('1')
  const handleSelect = (key: string, keyPath: string[]) => {
    console.log(key, keyPath)
  }
  </script>
  
  <style>
  .flex-grow {
    flex-grow: 1;
  }
  </style>
  
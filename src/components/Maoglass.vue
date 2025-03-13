<script setup lang="ts">
// 注意：在本示例中，实际上<script setup>部分并不需要任何内容，因为没有使用到Vue的响应式数据或方法
</script>

<template>
  <div>
    <p>使用<br />background-attachment: fixed<br />filter: blur()<br />实现毛玻璃效果</p>
  </div>
</template>

<style scoped lang="scss">
$imageUrl: 'https://images.unsplash.com/photo-1440688807730-73e4e2169fb8?dpr=1&auto=format&fit=crop&w=1500&h=1001&q=80&cs=tinysrgb&crop=';

html,
body {
  width: 100%;
  height: 100%;
  background-image: url(#{$imageUrl}); // 正确使用SCSS变量插入URL
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
  background-position: top;
  overflow: hidden;
}

div {
  position: relative;
  width: 30vw;
  height: 40vh;
  background: inherit;
  margin: 50px auto;
  padding: 5vmin;
  border-radius: 5px;
  border: 2px solid rgba(255, 255, 255, .5);

  p {
    position: relative;
    color: #000;
    z-index: 10;
    font-size: 24px;
    line-height: 1.5;
  }

  &::after {
    position: absolute;
    content: "";
    background: inherit;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    filter: blur(10px);
    z-index: -1; // 修正z-index，确保模糊层在底层
  }
}
</style>
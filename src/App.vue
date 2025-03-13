<script setup lang="ts">
    import banner1 from './assets/img/banner1.png'
    import banner2 from './assets/img/banner2.png'
    // import banner3 from './assets/img/d1.png'
    const imlist = [
    {url:banner1},
    {url:banner2},
    // {url:banner3}
]
import {
  ArrowRight,
  CaretBottom,
  CaretTop,
  Warning,
} from '@element-plus/icons-vue'
</script>

<template>
  <div id="app">
    <div class="header">
      <el-menu
        class="el-menu-demo"
        mode="horizontal"
        :ellipsis="false"
      >
      <el-menu-item index="0">
        <img src="./assets/logo2.png" width="128px"/>
        <!-- <p class="title">映彩智材</p> -->
      </el-menu-item>

      <el-menu-item index="1">首页</el-menu-item>
      <el-menu-item index="2">关于公司</el-menu-item>
      
      <el-menu-item index="3">产品技术</el-menu-item>
      <el-menu-item index="4">新闻中心</el-menu-item>
      <el-menu-item index="5">联系我们</el-menu-item>
    </el-menu>
  </div>


  </div>

  <div class="carousel-container">
    <!-- <div class="carousel">
    <el-carousel :interval="4000" type="card" height="200px">
    <el-carousel-item v-for="item in imlist" :key="item">
    <h3 text="2xl" justify="center"><img :src="item.url" alt=" " class="banner-imgs"></h3>
    </el-carousel-item>
    </el-carousel> -->

    <!-- <div class="block text-center">
    <span class="demonstration">
      Switch when indicator is hovered (default)
    </span>
    <el-carousel height="150px">
      <el-carousel-item v-for="item in imlist" :key="item">
        <h3 class="small justify-center" text="2xl"><img :src="item.url" alt=" " class="banner-imgs"></h3>
      </el-carousel-item>
    </el-carousel>
  </div> -->
  <div class="block-text-center" m="t-4">
    <span class="demonstration"></span>
    <el-carousel trigger="click" height="610px">
      <el-carousel-item v-for="item in imlist" :key="item">
        <h3 class="small justify-center" text="2xl">
          <img style="object-fit: fill; width:100%; height:100%;" :src="item.url" alt=" " class="banner-imgs" >
        </h3>
      </el-carousel-item>
    </el-carousel>
  </div>
  <!-- </div> -->
  <div class="statics">
    <el-row :gutter="16">
    <el-col :span="8">
      <div class="statistic-card">
        <el-statistic :value="2">
          <template #title>
            <div style="display: inline-flex; align-items: center">
              公司核心产品：
              <el-tooltip
                effect="dark"
                content="Number of users who logged into the product in one day"
                placement="top"
              >
                <el-icon style="margin-left: 4px" :size="12">
                  <Warning />
                </el-icon>
              </el-tooltip>
            </div>
          </template>
        </el-statistic>
        <div class="statistic-footer">
          <div class="footer-item">
            <!-- <span>than yesterday</span>
            <span class="green">
              24%
              <el-icon>
                <CaretTop />
              </el-icon>
            </span> -->
          </div>
        </div>
      </div>
    </el-col>
    <el-col :span="8">
      <div class="statistic-card">
        <el-statistic :value="1">
          <template #title>
            <div style="display: inline-flex; align-items: center">
              公司技术专利
              <el-tooltip
                effect="dark"
                content="Number of users who logged into the product in one month"
                placement="top"
              >
                <el-icon style="margin-left: 4px" :size="12">
                  <Warning />
                </el-icon>
              </el-tooltip>
            </div>
          </template>
        </el-statistic>
        <div class="statistic-footer">
          <div class="footer-item">
            <!-- <span>month on month</span>
            <span class="red">
              12%
              <el-icon>
                <CaretBottom />
              </el-icon>
            </span> -->
          </div>
        </div>
      </div>
    </el-col>
    <el-col :span="8">
      <div class="statistic-card">
        <el-statistic :value="2" title="New transactions today">
          <template #title>
            <div style="display: inline-flex; align-items: center">
              聘请专家顾问
            </div>
          </template>
        </el-statistic>
        <div class="statistic-footer">
          <div class="footer-item">
            <!-- <span>than yesterday</span>
            <span class="green">
              16%
              <el-icon>
                <CaretTop />
              </el-icon>
            </span> -->
          </div>
          <div class="footer-item">
            <el-icon :size="14">
              <ArrowRight />
            </el-icon>
          </div>
        </div>
      </div>
    </el-col>
  </el-row>
  </div>

  

  <div class="card-container">
    
    <!-- <el-card v-for="i in 4" :key="i" class="box-card" style="width: 400px">
      <template #header>
        <div class="card-header">
          <span>Card name</span>
          <el-button class="button" text>Operation button</el-button>
        </div>
      </template>
      <div v-for="o in 4" :key="o" class="text item">
        {{ 'List item ' + o }}
      </div>
    </el-card> -->
    <el-card style="width: 300px" class="cardimg1">
    <template #header>
      <h2>检测食品新鲜度</h2>
    </template>
    <img
      src="./assets/img/card1.jpg"
      style="width: 100% ; height: 250px"
    />
    <div>
      可检测食品腐败的酸性气体并产生颜色变化
    </div>
  </el-card>

  <el-card style="width: 300px" class="cardimg2">
    <template #header>
      <h2>抗紫外线</h2>
    </template>
    <img
      src="./assets/img/card2.jpg"
      style="width: 100%;height: 250px"
    />
    <div>
      在紫外线区,T280下降至小于10%
    </div>
  </el-card>

  <el-card style="width: 300px" class="cardimg3">
    <template #header>
      <h2>抑菌能力</h2>
    </template>
    <img
      src="./assets/img/card3.jpg"
      style="width: 100%;height: 250px"
    />
    <div>
      对白色念珠菌有显著抑制作用
    </div>
  </el-card>

  <el-card style="width: 300px" class="cardimg4">
    <template #header>
      <h2>绿色环保</h2>
    </template>
    <img
      src="./assets/img/card4.jpg"
      style="width: 100%;height: 250px"
    />
    <div>
      采用用天然着色剂,符合环境友好要求,可持续发展理念
    </div>
  </el-card>
  </div>

  <div class="THshow">
    <div class="textout">
   <div class="left" style="color:white">
    <br>
    <h1>最新产品</h1>
    <br>
    <h2>
      “瑞鲜膜”食品新鲜度监测标签
    </h2>
    <br>
<h3>
  “瑞鲜膜”可以检测到食品腐败释放的酸性气体，并通过自身的颜色变化将食品新鲜度可视化呈现；在使用方法、便携度上更加注重消费者的体验，满足客户需求；此产品通过引入天然着色剂等物质示色，绿色环保，无毒无害。
</h3>

   </div> 
  </div>
   <div>
    <img src="./assets/img/story.jpg" alt="" style="width: 900px">
   </div>
  </div>

  <div class="show-container">
    <div class="end">
      <div class="endone">
      <h3 style="color: aliceblue;">
      关于公司
      </h3>
        <h4 style="color: aliceblue;">公司简介</h4>
        <h4 style="color: aliceblue;">发展历程</h4>
        <h4 style="color: aliceblue;">发展战路</h4>
        <h4 style="color: aliceblue;">荣营资质</h4>
        <h4 style="color: aliceblue;">企业文化</h4>
        <h4 style="color: aliceblue;">新闻中心</h4>
        <h4 style="color: aliceblue;">技术创新</h4>
      </div>
      <div class="endtwo">
        <h3 style="color: aliceblue;">
          联系我们
      </h3>
      <h4 style="color: aliceblue;">
        人才招聘
      </h4>
        <h4 style="color: aliceblue;">招标中心</h4>
        <h4 style="color: aliceblue;">供应商入口</h4>
        <h4 style="color: aliceblue;">投资者关系</h4>
      </div >
        <div style="margin-left: 30px;">
      <h3 style="color: aliceblue;">
      映彩科技
      </h3>
        <h4 style="color: aliceblue;">技术发展</h4>
        <h4 style="color: aliceblue;">技术专利</h4>
        <h4 style="color: aliceblue;">未来展望</h4>
      </div>
      <div style="margin-left: 30px;">
      <h3 style="color: aliceblue;">
      产品中心
      </h3>
        <h4 style="color: aliceblue;">食品行业</h4>
        <h4 style="color: aliceblue;">检测行业</h4>
        <h4 style="color: aliceblue;">化工行业</h4>
        <h4 style="color: aliceblue;">智慧农业</h4>
        <h4 style="color: aliceblue;">环境质量检测</h4>
      </div>
    </div>
    <div>
        <img src="./assets/logo2.png" width="128px"/>
    </div>

  </div>
  </div>
  
  
</template>

<style lang="scss" scoped>
#app {
  position: relative; /* 用于正确定位内部的fixed元素 */
}

.container {
  min-height: 100vh; /* 使内容区域填满视口高度 */
}

.header {
  position: fixed; /* 添加此行使header固定在顶部 */
  top: 0;
  left: 0;
  right: 0; /* 让header占据整个宽度 */
  z-index: 999;
  display: flex;
  border-bottom: 1px solid #dddddd;
  padding: 0 20px;
  height: 56px;
  background-color: white; /* 可选，添加背景色以防内容被遮挡 */
}

.logo {
  height: 56px;
}

.title {
  font-size: 20px;
  font-weight: bold;
  margin-right: 88px;
  line-height: 56px;
  margin-left: 8px;
  color: var(--el-color-primary);
}

.main-content {
  padding-top: 56px; /* 避免与header重叠 */
  width: 100%;
}

.carousel-container {
  // width: 1300px;
  // height:500px;
  // display: flex;
  // justify-content: flex-start;
  position:absolute;
  top:0;
  right:0;
  bottom:0;
  left: 0;
  width: 100%;
  margin-top:10px;
}

.block-text-center{
  margin-top:50px;

}

.carousel{
  height: 300px;
  justify-content: center;
  align-items: center;
  width: 95%; 
  margin-bottom: 20px;
}

// 调整轮播项内部的文本样式以适应新的高度，如果需要的话
.el-carousel__item h3 {
line-height: 300px; // 这里假设我们增加了轮播图的高度至300px
}
.el-carousel__item h3 {
  color: #475669;
  opacity: 0.75;
  line-height: 200px;
  margin: 0;
  text-align: center;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}

.banner-imgs{
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.card-container{
  margin-top:50px;
  display: flex;
  justify-content: space-between;
}

.cardimg1{
  margin-left:20px;
  margin-bottom: auto;
}

.cardimg2{
  margin-top:80px;
  margin-bottom: auto;
}

.cardimg3{
  margin-left:30px;
  margin-bottom: auto;
}

.cardimg4{
  margin-top:80px;
  margin-right:20px;
  margin-bottom: auto;
}

.THshow{
  display: flex;
  margin-top:50px;
}

.left{
  margin-left:30px;
}
.show-container {
  width: 100%;
  height: 50vh;
  // color:red;
  background-image: linear-gradient(to right, #4CAF50, #99a9bf);
  background-size: cover;
}

:global(h2#card-usage ~ .example .example-showcase) {
  background-color: var(--el-fill-color) !important;
}

.el-statistic {
  --el-statistic-content-font-size: 28px;
}

.statistic-card {
  height: 100%;
  padding: 20px;
  border-radius: 4px;
  background-color: var(--el-bg-color-overlay);
}

.statistic-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  font-size: 12px;
  color: var(--el-text-color-regular);
  margin-top: 16px;
}

.statistic-footer .footer-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.statistic-footer .footer-item span:last-child {
  display: inline-flex;
  align-items: center;
  margin-left: 4px;
}

.green {
  color: var(--el-color-success);
}
.red {
  color: var(--el-color-error);
}
.statics{
  margin-top:50px;
}
.end{
  padding-top:30px;
  margin-left:30px;
  display: flex;
  // justify-content: space-evenly;
}
.endone{
  margin-left:30px;
}
.endtwo{
  margin-left:30px;
}
.textout{
  width:500px;
  height:auto;
  background-color:#99a9bf;
  margin-left:30px;
  margin-bottom:50px;
}
</style>

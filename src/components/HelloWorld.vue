<template>
  <div class="main" v-infinite-scroll="load">
    <el-card class="app-card" v-for="item in appListData">
      <template #header>
        <div class="app-card-header">
          <span>Tumblew</span>
          <el-image />
          <!-- <el-button class="button" text>Operation button</el-button> -->
        </div>
      </template>
      <el-button>安装</el-button>
      <el-button>扫码</el-button>
      <el-button>详情</el-button>
      <!-- <div v-for="o in 4" :key="o" class="text item">{{ 'List item ' + o }}</div> -->
    </el-card>
  </div>
  
</template>

<script>
  export default {
      data() {
          return {
              appListData: [
                "Tumblew",
                "Tumblew",
                "Tumblew",
                "Tumblew",
                "Tumblew",
                "Tumblew",
                "Tumblew",
                "Tumblew",
                "Tumblew",
                "Tumblew",
                "Tumblew",
                "Tumblew"
              ]
          }
      },
      methods: {
        load() {
          console.log("bottom-----bottom")
        }
      },
      //生命周期 - 创建完成,访问当前this实例
      created() {
          
      },
      //生命周期 - 挂载完成,访问DOM元素
      mounted() {
          
      }
  }
</script>

<style scoped>
/* @import url(); 引入css类 */

.main {
  width: calc(90vw + 20px);
  height: calc(100vh - 164px);
  padding-top: 25px;
  padding-bottom: 25px;
  margin: 0 auto;
  background-color: lightgray;
  display: grid;
  justify-content: space-evenly;
  grid-template-columns: repeat(auto-fill, 250px);
  grid-template-rows: repeat(auto-fill, 150px);
  grid-gap: 20px;
  gap: 20px;
  overflow: auto;
  
  -ms-overflow-style: none;
  scrollbar-width: none;

  border-radius: 5px;
}

.main::-webkit-scrollbar {
  display:none;/*隐藏滚动条*/
}

.app-card {
  width: 250px;
  height: 150px;
}

.app-card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>

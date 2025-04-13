<template>
  <div class="hello">
    <!-- <h2>Hello World</h2> -->
    <!-- 全屏容器 -->
    <dv-full-screen-container>
      <!-- <dv-loading>Loading...</dv-loading> -->
      <div class="module-box head-box">
        <dv-decoration-8 style="width:300px;height:50px;" />
        <dv-decoration-5 style="width:300px;height:40px;" />
        <dv-decoration-8 :reverse="true" style="width:300px;height:50px;" />
      </div>
      <div class="module-box">
        <!-- 左 -->
        <div style="flex: 0 1 25%;">
          <dv-border-box-8 style="width:100%;height:200px">
            <dv-capsule-chart :config="config1" style="width:100%;height:200px" />
          </dv-border-box-8>
          <dv-border-box-1 style="width:100%;height:200px">
            <dv-active-ring-chart :config="config3" style="width:100%;height:200px" />
          </dv-border-box-1>
        </div>
        <!-- 中 -->
        <div style="flex: 0 1 50%;">
          <dv-border-box-2 style="width:100%;height:400px">
            <dv-flyline-chart :config="config5" :dev="true" style="width:100%;height:100%;" />
          </dv-border-box-2>
        </div>
        <!-- 右 -->
        <div style="flex: 0 1 25%;">
          <dv-border-box-8 style="width:100%;height:200px">
            <dv-water-level-pond :config="config2" style="width:100%;height:200px" />
          </dv-border-box-8>
          <dv-border-box-1 style="width:100%;height:200px">dv-border-box-1</dv-border-box-1>
        </div>
      </div>
      <div class="module-box">
        <div style="flex: 0 1 50%;">
          <dv-border-box-9 style="width:100%;height:200px">
            <dv-scroll-ranking-board :config="config6" class="scroll-board" />
          </dv-border-box-9>
        </div>
        <div style="flex: 0 1 25%;">
          <dv-border-box-10 style="width:100%;height:200px">dv-border-box-1</dv-border-box-10>
        </div>
        <div style="flex: 0 1 25%;">
          <dv-border-box-13 style="width:100%;height:200px">dv-border-box-1</dv-border-box-13>
        </div>
      </div>
    </dv-full-screen-container>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
  return{
    config1:{
      data: [
        {
          name: '中国',
          value: 167
        },
        {
          name: '马来西亚',
          value: 123
        },
        {
          name: '柬埔寨',
          value: 98
        },
        {
          name: '韩国',
          value: 75
        },
        {
          name: '日本',
          value: 66
        }
      ],
      colors: ['#e062ae', '#fb7293', '#e690d1', '#32c5e9', '#96bfff'],
      unit: '单位'
    },
    config2:{
      data: [66, 45],
      shape: 'roundRect'
    },
    config3:{
      data: [
        {
          name: '中国',
          value: 80
        },
        {
          name: '日本',
          value: 2
        },
        {
          name: '韩国',
          value: 3
        },
        {
          name: '柬埔寨',
          value: 10
        },
        {
          name: '马来西亚',
          value: 5
        }
      ]
    },
    config4:{

    },
    config5:{
      centerPoint: [0.69, 0.51],
      points: [
        [0.20, 0.33],
        [0.19, 0.40],
        [0.26, 0.39],
        [0.32, 0.70],
        [0.77, 0.71],
        [0.81, 0.76],
        [0.53, 0.29],
        [0.70, 0.41],
        [0.72, 0.38],
        [0.75, 0.37],
        [0.44, 0.29],
        [0.54, 0.43],
        [0.68, 0.54],
        [0.68, 0.45],
        [0.73, 0.49],
        [0.68, 0.36],
        [0.46, 0.34]
      ],
      bgImgUrl: require('../assets//world.jpg')
    },
    config6:{
      data: [
        {
          name: '日本',
          value: 55
        },
        {
          name: '中国',
          value: 120
        },
        {
          name: '马来西亚',
          value: 78
        },
        {
          name: '新加坡',
          value: 66
        },
        {
          name: '柬埔寨',
          value: 80
        },
        {
          name: '泰国',
          value: 45
        },
        {
          name: '越南',
          value: 29
        }
      ]
    }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.module-box{
  display: flex;
  justify-content: space-between;
}
.scroll-board{
  width:94%;
  height:180px;
  margin: auto;
}
.head-box{
  padding: 10px;
}
</style>

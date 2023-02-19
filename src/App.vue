<template>
  <div id="app">
    <!-- 顶部导航栏 -->
    <div class="navigator">
      <!-- 导航栏左侧 -->
      <div class="nav-left">
        <p v-for="item in navList" :key="item.key">{{ item.name }}</p>
      </div>
      <!-- 导航栏右侧 -->
      <div class="nav-right">
        <p>登录</p>
        <p>注册</p>
        <p>消息通知</p>
        <div class="goodCar">
          购物车(0)
        </div>
      </div>
    </div>
    <div class="title">
      <div class="logo">
        <img src="./assets/小米logo.png" alt="">
      </div>
      <div class="title_list">
        <p v-for="item in titleList" :key="item.key">{{ item.name }}</p>
      </div>
      <div class="title-search">
        <input type="text" style="width:245px;height: 50px;box-sizing: border-box; vertical-align: middle;font-size: 15px;border: 1px solid #dcdcdc;border-right: none;" 
        placeholder="Redmi X Pro 65" />
        <button>Q</button>
      </div>
    </div>
    <div class="photo">
      <div></div>
      <div class="photo_top">
        <div class="photo_top_left">
          <div>
            <p></p>
          </div>
        </div>
        <div class="photo_top_right">

        </div>
      </div>
      <div class="photo_bottom">
        <div class="photo_bottom_left">
          <div v-for="item in divList" :key="item.key">
            <p>{{ item.name }}</p>
          </div>
        </div>
        <div class="photo_bottom_right">
          <img src="./assets/k60.png" alt="">
          <img src="./assets/xiaomi13.png" alt="">
          <img src="./assets/mix fold2.png" alt="">
        </div>
      </div>
      </div>
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <router-view/>
  </div>
</template>

<script>

export default {
  data() {
    return {
      navList: [
        {
          name: "小米官网",
          key: 0
        },
        {
          name: "小米商城",
          key: 1
        },
        {
          name: "MIUI",
          key: 2
        },
        {
          name: "loT",
          key: 3
        },
        {
          name: "云服务",
          key: 4
        },
        {
          name: "天星数科",
          key: 5
        },
        {
          name: "有品",
          key: 6
        },
        {
          name: "小爱开放平台",
          key: 7
        },
        {
          name: "企业团购",
          key: 8
        },
        {
          name: "资质证照",
          key: 9
        },
        {
          name: "协议规则",
          key: 10
        },
        {
          name: "下载App",
          key: 11
        },
        {
          name: "Select Location",
          key: 12
        },
      ],
      titleList: [
        {
          name: "Xiaomi手机",
          key: 0
        },
        {
          name: "Redmi手机",
          key: 1
        },
        {
          name: "电视",
          key: 2
        },
        {
          name: "笔记本",
          key: 3
        },
        {
          name: "平板",
          key: 4
        },
        {
          name: "家电",
          key: 5
        },
        {
          name: "路由器",
          key: 6
        },
        {
          name: "服务中心",
          key: 7
        },
        {
          name: "社区",
          key: 8
        }
      ],
      leftList: [
        {
          name: "手机",
          key: 0
        },
        {
          name: "电视",
          key: 1
        },
        {
          name: "家电",
          key: 2
        },
        {
          name: "笔记本 平板",
          key: 3
        },
        {
          name: "出行 穿戴",
          key: 4
        },
        {
          name: "耳机 音箱",
          key: 5
        },
        {
          name: "健康 儿童",
          key: 6
        }
      ],
      divList: [
        {
          name: "保障服务",
          key: 0
        },
        {
          name: "企业团购",
          key: 1
        },
        {
          name: "F码通道",
          key: 2
        },
        {
          name: "米粉卡",
          key: 3
        },
        {
          name: "以旧换新",
          key: 4
        },
        {
          name: "话费充值",
          key: 5
        }
      ]
    }
  }
}

</script>


<style scoped>
  /* 顶部导航样式 */
  .navigator {
  background-color: #2d2d2d;
  width: 100%;
  height: 40px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  }
  /* width: 1226px */
  .nav-left {
    margin-left: 340px;
    /* background-color: #fff; */
    display: flex;
    width: 790px;
    justify-content: space-around;
    color: #a5a5a5;
    border: 0;
  }

  .nav-right {
    /* background-color: #fff; */
    width: 375px;
    display: flex;
    justify-content: space-around;
    margin-right: 340px;
    margin-left: 61px;
    align-items: center;
    color: #a5a5a5;
    border: 0;
  }
  .goodCar {
    width: 230px;
    background-color: #3a3a3a;
    color: #a5a5a5;
    text-align: center;
    font-size: 12px;
    line-height: 40px;
  }

  .title {
    width: 1226px;
    margin-left: 340px;
    margin-top: 22px;
    margin-bottom: 22px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .title_list {
    display: flex;
    justify-content: space-around;
    align-items: center;
    width: 700px;
    font-size: 15px;
  }

  .title-search {
    height: 50px;
  }

  .title-search input {
    
  }

  .title-search button {
    /* vertical-align: middle; */
    height: 50px;
    width: 52px;
    background-color: #fff;
    border: 1px solid #dcdcdc;
  }

  .photo {
    width: 1226px;
    height: 644px;
    margin-left: 340px;
  }
/* height: 460px */
  .photo_top {
    height: 460px;
    width: 100%;
  }

  .photo_top_left {
    height: 100%;
    width: 324px;
    background-color: #9e9d9d;
  }

  .photo_bottom {
    margin-top: 14px;
    height: 170px;
    display: flex;
    justify-content: start;
  }

  .photo_bottom_left {
    height: 100%;
    width:324px;
    background: #544d46;
    color: #3a3a3a;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }

  .photo_bottom_left>div {
    width: 80px;
    height: 85px;
    border: 1px solid #5b534d;
  }

  .photo_bottom_left>div>p {
    color: #a5a5a5;
  }

  .photo_bottom_right {
    height: 100%;
    width: 902px;
    display: flex;
    justify-content: space-around;
    
  }
</style>

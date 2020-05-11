<template>
  <div class="container">
    <!-- 顶部 -->
    <myHeader></myHeader>
    <!-- 当前位置 -->
    <div class="location">
      <div class="current wrap">
        <div class="cur" v-for="(item,index) in dataList" :key="index">{{item.current}}</div>
      </div>
    </div>

    <!-- banner -->
    <nuxt-link to>
      <div class="banner" v-for="(item,index) in bannerList" :key="index">
        <img :src="item.imgurl" alt />
      </div>
    </nuxt-link>

    <!-- 企业补助 -->
    <div class="companies">
      <div class="comp wrap" v-for="(item,index) in titleList" :key="index">
        <div class="title">{{item.title}}</div>
        <div class="smtitle">{{item.smtitle}}</div>
      </div>

      <div class="wrap">
        <div class="teletext">
          <nuxt-link to v-for="(item,index) in teleList" :key="index">
            <div class="pic">
              <img :src="item.imgurl" alt />
            </div>

            <div class="text">{{item.text}}</div>
          </nuxt-link>
        </div>
      </div>
    </div>
    <!-- 底部 -->
    <!-- <myFooter></myFooter> -->
  </div>
</template>

<script>
import myHeader from "~/components/header.vue";
import myFooter from "~/components/footer.vue";
export default {
  components: {
    myHeader,
    myFooter
  },
  data() {
    return {
      dataList: [
        {
          current: "当前位置："
        },
        {
          current: "首页> "
        },
        {
          current: "政府支持"
        }
      ],
      bannerList: [
        {
          imgurl: require("~/static/政府补贴banner.png")
        }
      ],
      titleList: [
        {
          title: "企业补助",
          smtitle: "SUBSIDY"
        }
      ],
      teleList: [
        {
          id: 1,
          imgurl: require("~/static/hai.jpg"),
          text: "无锡"
        },
        {
          id: 2,
          imgurl: require("~/static/hai.jpg"),
          text: "泉州"
        },
        {
          id: 3,
          imgurl: require("~/static/hai.jpg"),
          text: "湖北"
        },
        {
          id: 4,
          imgurl: require("~/static/hai.jpg"),
          text: "杭州"
        },
        {
          id: 5,
          imgurl: require("~/static/hai.jpg"),
          text: "河南"
        },
        {
          id: 6,
          imgurl: require("~/static/hai.jpg"),
          text: "江西"
        },
        {
          id: 7,
          imgurl: require("~/static/hai.jpg"),
          text: "南通"
        },
        {
          id: 8,
          imgurl: require("~/static/hai.jpg"),
          text: "宁波"
        },
        {
          id: 9,
          imgurl: require("~/static/hai.jpg"),
          text: "上海"
        },
        {
          id: 10,
          imgurl: require("~/static/hai.jpg"),
          text: "苏州"
        },
        {
          id: 11,
          imgurl: require("~/static/hai.jpg"),
          text: "深圳"
        },
        {
          id: 12,
          imgurl: require("~/static/hai.jpg"),
          text: "广州"
        },
        {
          id: 13,
          imgurl: require("~/static/hai.jpg"),
          text: "福建"
        },
        {
          id: 14,
          imgurl: require("~/static/hai.jpg"),
          text: "安徽"
        },
        {
          id: 15,
          imgurl: require("~/static/hai.jpg"),
          text: "厦门"
        },
        {
          id: 16,
          imgurl: require("~/static/hai.jpg"),
          text: "惠州"
        }
      ]
    };
  }
};
</script>

<style scoped>
.location {
  background: #f4f6fb;
  height: 60px;
}
.location .cur {
  display: block;
  float: left;
  line-height: 60px;
}
.location .cur:last-child {
  color: #2c8ffe;
}

.banner {
  width: 1920px;
  height: 400px;
  position: relative;
  left: 50%;
}

.banner img {
  position: absolute;
  top: 0;
  margin-left: -50%;
}

.companies {
  width: 100%;
  background: #f4f5fb;
}
.comp {
  padding-top: 26px;
}
.comp .title {
  color: #333333;
  font-size: 34px;
  font-weight: normal;
  margin-bottom: 15px;
  text-align: center;
}
.comp .smtitle {
  color: #333333;
  font-size: 14px;
  margin-bottom: 44px;
  text-align: center;
}

.teletext {
  display: flex;
  flex-wrap: wrap;
  position: absolute;
}

.pic img {
  width: 130px;
  height: 130px;
  border-radius: 60px;
  margin-right: 23px;
}
.text {
  font-size: 20px;
  color: red;
  position: relative;
  top: -70px;
  left: 46px;
}
</style>
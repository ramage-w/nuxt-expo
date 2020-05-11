<template>
  <div class="container">
    <!-- 顶栏 -->
     <myHeader></myHeader>
    <!-- 中间的部分 -->
    <div class="main">
      <div class="nav">
        <div class="nav_left">
          <ul>
            <li>
              <div class="text">产品服务</div>
            </li>
            <li>
              <div class="navbox">
                <img src="../img/国外展会.png" alt />
                <div class="navname">
                  <a href="#">国外展会</a>
                </div>
              </div>
            </li>
            <li>
              <div class="navbox">
                <img src="../img/国内展会.png" alt />
                <div class="navname">
                  <a href="#">国内展会</a>
                </div>
              </div>
            </li>
            <li>
              <div class="navbox">
                <img src="../img/360商城.png" alt />
                <div class="navname">
                  <a href="#">360商城</a>
                </div>
              </div>
            </li>
            <li>
              <div class="navbox">
                <img src="../img/数字展览.png" alt />
                <div class="navname">
                  <a href="#">数字展览</a>
                </div>
              </div>
            </li>
            <li>
              <div class="navbox">
                <img src="../img/爱采购.png" alt />
                <div class="navname">
                  <a href="#">爱采购</a>
                </div>
              </div>
            </li>
            <li>
              <div class="navbox">
                <img src="../img/360人资.png" alt />
                <div class="navname">
                  <a href="#">360人资</a>
                </div>
              </div>
            </li>
            <li>
              <div class="navbox">
                <img src="../img/全球搜.png" alt />
                <div class="navname">
                  <a href="#">全球搜</a>
                </div>
              </div>
            </li>
            <li>
              <div class="navbox">
                <img src="../img/品牌战略.png" alt />
                <div class="navname">
                  <a href="#">品牌战略</a>
                </div>
              </div>
            </li>
          </ul>
        </div>
        <div class="nav_right">
          <div class="banner">
            <img src="../img/banner.png" alt />
            <img src alt />
            <img src alt />
            <img src alt />
          </div>
        </div>
      </div>
    </div>

    <!-- 图文混排 1-->
    <div style="background:#f8f8f8">
      <div class="title clearfix">
        <div class="tw" v-for="(item,index) in dataList" :key="index">
          <div class="pic">
            <img :src="item.img" alt />
          </div>
          <div class="text">
            <h4>{{item.title}}</h4>
            <p>{{item.contain}}</p>
            <span>{{item.base}}</span>
          </div>
        </div>
      </div>
    </div>
    <!-- 图文混排 2-->
    <div style="background:#fff">
      <div class="title">
        <div class="title clearfix">
          <div class="tw" v-for="(item,index) in titleList" :key="index">
            <div class="pic">
              <img :src="item.img" alt />
            </div>
            <div class="text">
              <h4>{{item.title}}</h4>
              <p>{{item.contain}}</p>
              <span>{{item.base}}</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 底部图片 -->
    <div class="bttom_bg">
      <img src="../img/xiaobanner.png" alt />
      <nuxt-link to="/" class="btn">欢迎加盟</nuxt-link>
    </div>
    <myFooter></myFooter>
  </div>
</template>

<script>
import myHeader from "~/components/header.vue"
import myFooter from "~/components/footer.vue";

export default {
  
  data() {
    return {
      dataList: [
        {
          img: require("../img/pic.jpg"),
          title: "国外展会",
          contain: "搭建中小企业走向世界的桥梁",
          base: "lEARN MORE"
        },
        {
          img: require("../img/pic.jpg"),
          title: "国内展会",
          contain: "构建会展综合服务链",
          base: "lEARN MORE"
        },
        {
          img: require("../img/pic.jpg"),
          title: "数字展览",
          contain: "云参展、云观展一站式服务",
          base: "lEARN MORE"
        },
        {
          img: require("../img/pic.jpg"),
          title: "360商城",
          contain: "进出口展品交易商城",
          base: "lEARN MORE"
        }
      ],
      titleList: [
        {
          img: require("../img/pic.jpg"),
          title: "全球搜",
          contain: "企业网站定制化建设",
          base: "lEARN MORE"
        },
        {
          img: require("../img/pic.jpg"),
          title: "360人资",
          contain: "传承世博大学智慧和文化",
          base: "lEARN MORE"
        },
        {
          img: require("../img/pic.jpg"),
          title: "品牌战略",
          contain: "品牌综合体系构建者",
          base: "lEARN MORE"
        },
        {
          img: require("../img/pic.jpg"),
          title: "爱采购",
          contain: "生意从此做起",
          base: "lEARN MORE"
        }
      ]
    };
  },
  components: {
     myHeader,
    myFooter
  },
};
</script>

<style scoped>

.clearfix:after {
  clear: both;
  content: ".";
  height: 0px;
  font-size: 0px;
  overflow: hidden;
  display: block;
}

.main {
  width: 100%;
  height: 722px;
  background: linear-gradient(
    54deg,
    rgba(31, 162, 255, 1) 0%,
    rgba(18, 216, 250, 1) 100%
  );
  margin-top: 10px;
  overflow: hidden;
}
.nav {
  width: 1200px;
  height: 722px;
  margin: 40px auto;
}
.nav_left {
  width: 270px;
  height: 640px;
  background: rgba(255, 255, 255, 1);
  box-shadow: 0px 1px 18px 0px rgba(0, 12, 26, 0.14);
  float: left;
}
.nav_left ul {
  width: 100%;
  height: 100%;
}
.nav_left ul li {
  height: 70px;
  line-height: 70px;
}
.nav_left ul li .text {
  text-align: left;
  text-indent: 10px;
  color: #333333ff;
  height: 50px;
  line-height: 50px;
  border-bottom: 1px solid #ebebebff;
}
.nav_left .navbox img {
  width: 30px;
  height: 30px;
  float: left;
  display: inline;
  margin-top: 20px;
  margin-left: 29px;
}
.nav_left .navname a {
  color: #333333ff;
  font-weight: normal;
  display: inline;
  margin-left: 22px;
}
.nav_right {
  float: left;
}
.nav_right .banner img {
  width: 930px;
  height: 640px;
}
.title {
  width: 1200px;
  margin: auto;
  padding-top: 73px;
}

.tw {
  float: left;
  padding-right: 15px;
}
.tw .pic img {
  width: 285px;
  height: 328px;
  overflow: hidden;
}
.text {
  height: 170px;
  text-align: center;
  background: #fff;
  margin-bottom: 47px;
}
.text h4 {
  padding-top: 20px;
  margin-bottom: 32px;
  height: 20px;
  font-size: 20px;
  font-weight: normal;
  color: #333333ff;
  line-height: 20px;
}
.text p {
  margin-top: 12px;
  margin-bottom: 49px;
  color: #666666ff;
  font-size: 16px;
  height: 16px;
  line-height: 16px;
}
.text span {
  width: 150px;
  height: 56px;
  border: 1px solid #2c8ffeff;
  padding: 21px 25px;
  color: #2c8ffeff;
}
.bttom_bg {
  width: 1920px;
  height: 250px;
  position: relative;
  left: 50%;
}
.bttom_bg img {
  width: 1920px;
  height: 250px;
  position: absolute;
  top: 0;
  margin-left: -960px;
  display: block;
  border: none;
  z-index: 2;
}
.btn {
  width: 160px;
  height: 44px;
  z-index: 3;
  position: absolute;
  top: 172px;
  left: -80px;
  display: block;
  background: #fff;
  color: #2c8ffe;
  font-size: 16px;
  text-align: center;
  line-height: 44px;
}
</style>

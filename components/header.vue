<template>
  <div class="header-wrapper">
    <div class="wrap head-top">
      <div class="head-top-left">
        欢迎您！进入
        <nuxt-link class="head-top-left-link" to="/">中企世博</nuxt-link>官网
      </div>
      <div class="head-to-right">
        服务电话：
        <span>6666-8888</span>
      </div>
    </div>
    <div class="wrap head">
      <nuxt-link to="/" class="logo">
        <img :src="Logo" alt />
      </nuxt-link>
      <div class="nav">
        <div class="nav-item" v-for="(item, index) in navList" :key="index">
          <nuxt-link class="nav-item-link" v-if="!item.hasSelect" :to="item.link">{{item.name}}</nuxt-link>
          <div class="nav-select" v-else>
            <span class="nav-select-title">{{item.name}}</span>
            <div class="select-wrap">
              <nuxt-link
                class="select-link"
                v-for="(selectItem, selectIndex) in item.children"
                :key="selectIndex"
                :to="selectItem.link"
              >{{selectItem.name}}</nuxt-link>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "my-header",
  props: {},
  data() {
    return {
      Logo: require("~/img/logo.png"),
      navList: [
        {
          name: "首　页",
          link: "/",
          hasSelect: false
        },
        {
          name: "客户服务",
          link: "",
          hasSelect: true,
          children: [
            {
              name: "创意视频",
              link: "/"
            },
            {
              name: "品牌战略",
              link: "/"
            },
            {
              name: "网站建设",
              link: "/"
            },
            {
              name: "展会服务",
              link: "/"
            }
          ]
        },
        {
          name: "新闻中心",
          link: "",
          hasSelect: true,
          children: [
            {
              name: "社会新闻",
              link: "/"
            },
            {
              name: "公司新闻",
              link: "/"
            }
          ]
        },
        {
          name: "战略合作",
          link: "",
          hasSelect: true,
          children: [
            {
              name: "阿里合作",
              link: "/"
            },
            {
              name: "腾讯合作",
              link: "/"
            }
          ]
        },
        {
          name: "集团风采",
          link: "/",
          hasSelect: false
        }
      ]
    };
  },
  created() {},
  mounted() {},
  methods: {},
  computed: {},
  watch: {}
};
</script>

<style scoped>
.header-wrapper {
  width: 100%;
  background: #fff;
}
.head-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  line-height: 40px;
  font-size: 12px;
}
.head-top-left .head-top-left-link {
  color: #204066;
  font-size: 12px;
}
.head-to-right span {
  font-size: 14px;
  color: #204066;
  font-weight: bold;
}
.head {
  margin-top: 20px;
  display: flex;
  justify-content: space-between;
  padding-bottom: 12px;
}
.nav {
  display: block;
  display: flex;
  align-items: center;
}
.nav .nav-item {
  font-size: 16px;
  margin-left: 60px;
  cursor: pointer;
  transition: 0.3s;
}
.nav .nav-item:hover {
  color: #2c8ffe;
}
.nav .nav-item .nav-item-link {
  font-size: 16px;
  color: #333;
  transition: 0.3s;
}
.nav-select-title {
  position: relative;
  display: block;
}
.nav-select-title::after {
  content: "";
  display: block;
  background: url("~static/select.png") center no-repeat;
  width: 12px;
  height: 8px;
  position: absolute;
  right: -14px;
  top: 12px;
  transition: 0.3s;
}
.nav .nav-item:hover .nav-select-title::after {
  background: url("~static/select-hover.png") center no-repeat;
}
.nav .nav-item:hover .nav-item-link {
  color: #2c8ffe;
}
.nav-item .nav-select {
  position: relative;
  height: 30px;
  line-height: 30px;
}
.nav-select .select-wrap {
  width: 100px;
  height: auto;
  position: absolute;
  left: 50%;
  margin-left: -50px;
  top: 30px;
  background: #fff;
  box-shadow: 2px 1px 10px 0px rgba(0, 12, 26, 0.1);
  border-radius: 4px;
  overflow: hidden;
  height: 0;
  transition: .5s;
  z-index: 10;
}
.nav-select .select-wrap .select-link {
  display: block;
  text-align: center;
  line-height: 40px;
  transition: .3s;
  font-size: 14px;
  color: #333;
}
.nav-select .select-wrap .select-link:hover {
  color: #2c8ffe;
}
.nav .nav-item:hover .nav-select .select-wrap {
  height: auto;
  padding: 10px 0;
}
</style>

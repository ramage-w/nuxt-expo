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

    <!-- 战略合作 -->
    <div class="partn">
      <nuxt-link to class="pr wrap">
        <div class="pic" v-for="(item,index) in picList" :key="index">
          <div class="item_pic">
            <img :src="item.imgurl" alt />
          </div>
          <div class="text">{{item.text}}</div>
        </div>
      </nuxt-link>
    </div>

    <!-- 分页器 -->
    <div class="paging wrap flexbox">
      <div class="flexbox">
        <div class="ud mr">上一页></div>

        <div class="he mr">首页</div>
      </div>

      <div class="pag flexbox mr">
        <div class="fy mr" v-for="(item,index) in pageList" :key="index">{{item.num}}</div>
      </div>

      <div class="flexbox">
        <div class="ud mr">下一页></div>
        <div class="he mr">尾页</div>
      </div>
    </div>

    <!-- 底部 -->
    <myFooter></myFooter>
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
          current: "战略合作>"
        },
        {
          current: "媒体支持"
        }
      ],
      picList: [
        {
          id: 1,
          imgurl: require("~/static/logo.png"),
          text: "中华人民共和国商务部"
        },
        {
          id: 2,
          imgurl: require("~/static/logo.png"),
          text: "中华人民共和国商务部"
        },
        {
          id: 3,
          imgurl: require("~/static/logo.png"),
          text: "中华人民共和国商务部"
        },
        {
          id: 4,
          imgurl: require("~/static/logo.png"),
          text: "中华人民共和国商务部"
        },
        {
          id: 5,
          imgurl: require("~/static/logo.png"),
          text: "中华人民共和国商务部"
        },
        {
          id: 6,
          imgurl: require("~/static/logo.png"),
          text: "中华人民共和国商务部"
        },
        {
          id: 7,
          imgurl: require("~/static/logo.png"),
          text: "中华人民共和国商务部"
        },
        {
          id: 8,
          imgurl: require("~/static/logo.png"),
          text: "中华人民共和国商务部"
        },
        {
          id: 9,
          imgurl: require("~/static/logo.png"),
          text: "中华人民共和国商务部"
        },
        {
          id: 10,
          imgurl: require("~/static/logo.png"),
          text: "中华人民共和国商务部"
        },
        {
          id: 11,
          imgurl: require("~/static/logo.png"),
          text: "中华人民共和国商务部"
        }
      ],
      pageList: [
        {
          num: "1"
        },
        {
          num: "2"
        },
        {
          num: "3"
        },
        {
          num: "4"
        },
        {
          num: "5"
        },
        {
          num: "6"
        },
        {
          num: "7"
        },
        {
          num: "8"
        },
        {
          num: "9"
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
.partn {
  width: 100%;
  background: #f4f6fb;
}
.pr {
  display: flex;
  flex-wrap: wrap;
  background: #f4f6fb;
  padding-top: 16px;
  justify-content: space-between;
}
.pic {
  width: 285px;
  /* display: block; */

  margin-bottom: 15px;
}
.pic .item_pic {
  width: 285px;
  height: 171px;
  background: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}
.pic img {
  max-width: 100%;
  max-height: 100%;
}
.pic .text {
  line-height: 40px;
  text-align: center;
  color: #333;
  font-size: 16px;
}

.paging {
  margin-top: 26px;
  margin-bottom: 36px;
  color: #666666;
  flex-direction: row-reverse;
  cursor: pointer;
}

.fy {
  width: 35px;
  height: 35px;
  background: rgba(255, 255, 255, 1);
  border: 1px solid rgba(229, 229, 229, 1);
  border-radius: 3px;
  text-align: center;
  line-height: 35px;
}
.fy:hover {
  border: 1px solid #2c8ffe;
  color: #2c8ffe;
}
.flexbox {
  display: flex;
  align-items: center;
}
.flexbox {
  display: flex;
  align-items: center;
}
.mr {
  margin-right: 8px;
}
.ud {
  width: 65px;
  height: 35px;
  background: rgba(255, 255, 255, 1);
  border: 1px solid rgba(229, 229, 229, 1);
  border-radius: 3px;
  text-align: center;
  line-height: 35px;
}
.ud:hover {
  border: 1px solid #2c8ffe;
  color: #2c8ffe;
}
.he {
  width: 50px;
  height: 35px;
  background: rgba(255, 255, 255, 1);
  border: 1px solid rgba(229, 229, 229, 1);
  border-radius: 3px;
  text-align: center;
  line-height: 35px;
}
.fy:hover {
  border: 1px solid #2c8ffe;
  color: #2c8ffe;
}
</style>
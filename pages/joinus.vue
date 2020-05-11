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
    <div class="banner" v-for="(item,index) in bannerList" :key="index">
      <img :src="item.imgurl" alt />
    </div>

    <!-- 加入我们 -->
    <div class="joinus">
      <div class="join wrap" v-for="(item,index) in titleList" :key="index">
        <div class="title">{{item.title}}</div>
        <div class="smtitle">{{item.smtitle}}</div>

        <div class="tab">
          <div class="tablt-box">
            <div 
              class="tablt" 
              v-for="(item,index) in tabList"
              :key="index" @click="cutTab(index)"
              :class="cutindex==index?'cutactive':''"
            >{{item.text}}</div>
          </div>

          <div class="tabrt">
              <el-table :data="tableData" style="width: 100%">
                <el-table-column prop="date" label="职位名称" width="180"></el-table-column>
                <el-table-column prop="name" label="职位类别" width="180"></el-table-column>
                <el-table-column prop="address" label="地点"></el-table-column>
                <el-table-column prop="text" label="详情"> <nuxt-link class="a" to="">查看详情 </nuxt-link> </el-table-column> 
              </el-table>

          </div>
        </div>
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
          current: "集团风采>"
        },
        {
          current: "加入我们"
        }
      ],

      cutindex:'0',

      bannerList: [
        {
          imgurl: require("~/img/join.png")
        }
      ],
      titleList: [
        {
          title: "加入我们",
          smtitle: "JOIN US"
        }
      ],
      tabList: [
        {
          text: "销售/服务"
        },
        {
          text: " 技术/研发"
        },
        {
          text: " 营销公关"
        },
        {
          text: " 战略投资"
        },
        {
          text: "人力资源"
        }
      ],
        tableData: [{
          date: '销售精英',
          name: '销售/服务',
          address: '郑州',
          text:"详情"
        }, {
          date: '销售精英',
          name: '销售/服务',
          address: '郑州',
          text:"详情"
        }
        ]
    };
  },
  methods:{
    cutTab:function(even){
      console.log(even);
      this.cutindex = even;
    }
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
.joinus {
  width: 100%;
  background: #f4f6fb;
}
.join {
  padding: 26px 0 79px;
}
.join .title {
  color: #333333;
  font-size: 34px;
  font-weight: normal;
  margin-bottom: 15px;
  text-align: center;
}
.join .smtitle {
  color: #666666;
  font-size: 14px;
  margin-bottom: 35px;
  text-align: center;
}

.tab {
  display: flex;
  align-items: center;
}
.tab .tablt-box {
  width: 280px;
  height: 641px;

}
.tab .tablt {
  width: 280px;
  height: 60px;
  text-align: center;
  line-height: 60px;
  border-bottom: 1px solid #ebebec;
  color: #333333;
  font-size: 20px;
}

.tab .tablt:hover{
  cursor: pointer;
  }
.tab .tabrt {
  width: 920px;
  height: 641px;
  background:#ffff;
}


.tab .cutactive{
  color: #2C8FFE;
  background: #fff;
}

</style>


<style>
.el-table tr {
  height: 60px;
}
.has-gutter th{
  text-align: center;
  color:#333333;
  font-size: 20px;
}

.a{
  color: #2C8FFE;
  font-size: 16px;
  text-decoration:underline;
}
.el-table .cell {
  color: #666666;
  text-align: center;
  font-size: 16px;
}
</style>
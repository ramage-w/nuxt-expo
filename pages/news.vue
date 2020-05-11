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
    <!-- 正文文本 -->
    <div class="text wrap">
     <div class="borbot" v-for="(item,index) in textList" :key="index">
       <nuxt-link 
          v-for="(itemlist,indexlist) in item.list" 
          :key="indexlist" 
          to=""
          class="text1"
        >
            <div>{{itemlist.text}}</div>
            <div>{{itemlist.time}}</div> 
        </nuxt-link>
     </div>  
    </div>
    <!-- 分页器 -->
    <div class="paging wrap flexbox">
      <div class="flexbox">
        <div class="ud mr">上一页></div>

        <div class="he mr">首页</div>
      </div>

      <div class="pag flexbox mr">
        <div class="fy mr" v-for="(item,index) in pageList" :key="index">
          {{item.num}}
        </div>
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
          current: "新闻中心>"
        },
        {
          current: "企业新闻"
        }
      ],
      textList: [
        {
          list:[
            {
              text: "佛山市企业参加国内专业展会补贴申报已开始 ",
              time: "2020-04-01"
            },
            {
              text: "2018上半年深圳市境外展会补贴政",
              time: "2020-04-01"
            },
            {
              text: "  小贴士展览：如何寻找方法来改进自己的展",
              time: "2020-04-01"
            },
            {
              text: " 展会基本知识:规则和技",
              time: "2020-04-01"
            },
            {
              text: " 前所未有的贸易展营销解决方",
              time: "2020-04-01"
            }
          ]
        },
        {
          list:[
            {
              text: "佛山市企业参加国内专业展会补贴申报已开始 ",
              time: "2020-04-01"
            },
            {
              text: "2018上半年深圳市境外展会补贴政",
              time: "2020-04-01"
            },
            {
              text: "  小贴士展览：如何寻找方法来改进自己的展",
              time: "2020-04-01"
            },
            {
              text: " 展会基本知识:规则和技",
              time: "2020-04-01"
            },
            {
              text: " 前所未有的贸易展营销解决方",
              time: "2020-04-01"
            }
            
          ]
        },
         {
          list:[
            {
              text: "佛山市企业参加国内专业展会补贴申报已开始 ",
              time: "2020-04-01"
            },
            {
              text: "2018上半年深圳市境外展会补贴政",
              time: "2020-04-01"
            },
            {
              text: "  小贴士展览：如何寻找方法来改进自己的展",
              time: "2020-04-01"
            },
            {
              text: " 展会基本知识:规则和技",
              time: "2020-04-01"
            },
            {
              text: " 前所未有的贸易展营销解决方",
              time: "2020-04-01"
            }
            
          ]
        },
         {
          list:[
            {
              text: "佛山市企业参加国内专业展会补贴申报已开始 ",
              time: "2020-04-01"
            },
            {
              text: "2018上半年深圳市境外展会补贴政",
              time: "2020-04-01"
            },
            {
              text: "  小贴士展览：如何寻找方法来改进自己的展",
              time: "2020-04-01"
            },
            {
              text: " 展会基本知识:规则和技",
              time: "2020-04-01"
            },
            {
              text: " 前所未有的贸易展营销解决方",
              time: "2020-04-01"
            }
            
          ]
        },
         {
          list:[
            {
              text: "佛山市企业参加国内专业展会补贴申报已开始 ",
              time: "2020-04-01"
            },
            {
              text: "2018上半年深圳市境外展会补贴政",
              time: "2020-04-01"
            },
            {
              text: "  小贴士展览：如何寻找方法来改进自己的展",
              time: "2020-04-01"
            },
            {
              text: " 展会基本知识:规则和技",
              time: "2020-04-01"
            },
            {
              text: " 前所未有的贸易展营销解决方",
              time: "2020-04-01"
            }
            
          ]
        },
         {
          list:[
            {
              text: "佛山市企业参加国内专业展会补贴申报已开始 ",
              time: "2020-04-01"
            },
            {
              text: "2018上半年深圳市境外展会补贴政",
              time: "2020-04-01"
            },
            {
              text: "  小贴士展览：如何寻找方法来改进自己的展",
              time: "2020-04-01"
            },
            {
              text: " 展会基本知识:规则和技",
              time: "2020-04-01"
            },
            {
              text: " 前所未有的贸易展营销解决方",
              time: "2020-04-01"
            }
            
          ]
        },
         {
          list:[
            {
              text: "佛山市企业参加国内专业展会补贴申报已开始 ",
              time: "2020-04-01"
            },
            {
              text: "2018上半年深圳市境外展会补贴政",
              time: "2020-04-01"
            },
            {
              text: "  小贴士展览：如何寻找方法来改进自己的展",
              time: "2020-04-01"
            }
          ]
        }
        
      ],
      pageList:[
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
  margin-bottom:29px;
}
.location .cur {
  display: block;
  float: left;
  line-height: 60px;
}
.location .cur:last-child{
  color: #2C8FFE;
}
.text .text1{
  font-size: 16px;
  color: #666666;
  display: flex;
  align-items: center;
  justify-content: space-between;
  line-height: 25px;
}
.text .borbot{
  border-bottom: 1px solid #EBEBEC;
  padding: 21px 0;
}
.text .text1:hover{
  color:  #2C8FFE;
  font-weight: bold;
}
.text .borbot:last-child{
  border-bottom: none; 
}
.paging{
  margin-bottom: 53px;
  color:#666666;
  flex-direction: row-reverse;
  cursor: pointer;
}

.fy{
  width:35px;
  height:35px;
  background:rgba(255,255,255,1);
  border:1px solid rgba(229,229,229,1);
  border-radius:3px;
  text-align: center;
  line-height:35px;
}
.fy:hover{
  border:1px solid #2C8FFE;
  color: #2C8FFE;
}
.flexbox{
  display: flex;
  align-items: center; 
}
.flexbox{
  display: flex;
  align-items: center; 
}
.mr{
  margin-right: 8px;
} 
.ud{
  width:65px;
  height:35px;
  background:rgba(255,255,255,1);
  border:1px solid rgba(229,229,229,1);
  border-radius:3px;
  text-align: center;
  line-height:35px;
}
.ud:hover{
  border:1px solid #2C8FFE;
  color: #2C8FFE;
}
.he{
  width:50px;
  height:35px;
  background:rgba(255,255,255,1);
  border:1px solid rgba(229,229,229,1);
  border-radius:3px;
  text-align: center;
  line-height:35px;
}
.fy:hover{
  border:1px solid #2C8FFE;
  color: #2C8FFE;
}
</style>

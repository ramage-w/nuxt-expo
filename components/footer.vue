<template>
  <!-- 合作伙伴 -->
  <div class="partner">
    <div class="part">
      <div class="aa" v-for="(item, index) in textList" :key="index">
        <div class="aa-title">{{item.name}}</div>
        <div class="bb">
          <nuxt-link
            class="bb-item"
            v-for="(childItem,childIndex) in item.children"
            :key="childIndex"
            :to="childItem.link"
          >{{childItem.name}}</nuxt-link>
        </div>
      </div>
    </div>
    <div class="contact">
      <div class="tel">联系我们</div>
      <div>电话：010-69235235</div>
      <div class="yx">邮箱：010-69235235</div>
      <div class="addr">地址:</div>
      <div>北京大兴区滨河路27号</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      textList: [
        {
          name: "中企世博",
          children: [
            {
              id: 1,
              name: "关于我们",
              link: "/"
            },
            {
              id: 1,
              name: "企业动态",
              link: "/"
            },
            {
              id: 1,
              name: "合作伙伴",
              link: "/"
            }
          ]
        },
        {
          name: "中企产业",
          children: [
            {
              id: 1,
              name: "境外展会",
              link: "/"
            },
            {
              id: 1,
              name: "国内展会",
              link: "/"
            },
            {
              id: 1,
              name: "数字展览",
              link: "/"
            },
            {
              id: 1,
              name: "360商城",
              link: "/"
            },
            {
              id: 1,
              name: "全球搜",
              link: "/"
            },
            {
              id: 1,
              name: "360人资",
              link: "/"
            },
            {
              id: 1,
              name: "跨境通",
              link: "/"
            },
            {
              id: 1,
              name: "爱采购",
              link: "/"
            }
          ]
        },
        {
          name: "集团风采",
          children: [
            {
              id: 1,
              name: "政府支持",
              link: "/"
            },
            {
              id: 1,
              name: "世博大学",
              link: "/"
            },
            {
              id: 1,
              name: "中企月刊",
              link: "/"
            }
          ]
        },
        {
          name: "加入我们",
          children: [
            {
              id: 1,
              name: "校园加盟",
              link: "/"
            },
            {
              id: 1,
              name: "社会招聘",
              link: "/"
            },
            {
              id: 1,
              name: "企业文化",
              link: "/"
            }
          ]
        }
      ]
    };
  }
};
</script>

<style scoped>
.partner {
  width: 100%;
  height: 577px;
  background: #222934ff;
  color: #fff;
  padding-top: 90px;
}
.partner .aa {
  float: left;
  margin-right: 121px;
}
.partner .part {
  width: 1200px;
  margin: auto;
}
.partner .part .aa-title {
  font-size: 16px;
}
.partner .part .bb-item {
  color: #fff;
  display: block;
  font-size: 14px;
  font-weight: normal;
  margin: 30px 0px;
}
.contact {
  font-size: 14px;
  float: left;
}
.yx {
  margin-top: 12px;
}
.tel {
  font-size: 16px;
  margin-bottom: 30px;
}
.addr {
  margin: 30px 0 15px;
}
</style>
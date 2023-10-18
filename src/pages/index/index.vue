<!-- <template>
  <view class="content"> -->
    <!-- <image class="logo" src="/static/logo.png" /> -->
    <!-- <swiper current="1" class="text-area">
      <swiper-item key="1" class="title">
        <view class="item"></view>
      </swiper-item>
      <swiper-item key="3" class="title"><img src="/static/logo.png" /></swiper-item>
    </swiper>
  </view> -->
<!-- </template> -->
<!-- 
<script setup lang="ts">
import { ref } from 'vue'
const title = ref('Hello')
</script> -->

<!-- <style>
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200rpx;
  width: 200rpx;
  margin-top: 200rpx;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 50rpx;
}
.item {
  width: 200rpx;
  height: 200rpx;
  margin-left: auto;
  margin-right: auto;
  border: 1px solid red;
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36rpx;
  color: #8f8f94;
}
</style> -->
<template>
  <swiper class="swiper"
          previous-margin="60rpx"
          next-margin="40rpx"
          circular="true"
          @change="showSwiperItem"
  >
    <swiper-item>
      <view class="swiper-item">
        <view class="head">
          <img src="../../static/v2.1/expert-avatar-yuelin.png" class="avatar"/>
          <text class="name">岳林</text>
        </view>
        <view class="card" :class="{activate: currentItem === 0}">
          <text>
            主任医师、教授、博士生导师。曾于英国Unilever牙科研究所和美国The Forsyth Institute进行研究工作。一直工作在牙体牙髓病学临床、教学与科研第一线，临床经验丰富。获省部级奖6项，发表学术论文100余篇，主编主译著作6部，主编北大教材＂牙体牙髓病学＂，参编著作20余部。
          </text>
        </view>
      </view>
    </swiper-item>
    <swiper-item>
      <view class="swiper-item">
        <view class="head">
          <img src="../../static/v2.1/expert-avatar-liangyuhong.png" class="avatar"/>
          <text class="name">梁宇红</text>
        </view>
        <view class="card" :class="{activate: currentItem === 1}">
          <text>
            北京大学国际医院口腔科主任，教授。1993年毕业于北京大学口腔医院，获得学士学位；2004年获得医学博士学位。并于荷兰自由大学／阿姆斯特丹大学牙科研究中心获得PhD学位。梁宇红医生在牙髓病学方面具有丰富的经验。现担任中华牙体牙髓病学专委会常务委员，并在北京大学口腔医院兼职担任教授和主任医师，开展毕业后临床培训和教育。
          </text>
        </view>
      </view>
    </swiper-item>
    <swiper-item>
      <view class="swiper-item">
        <view class="head">
          <img src="../../static/v2.1/expert-avatar-anyu.png" class="avatar"/>
          <text class="name">安钰</text>
        </view>
        <view class="card" :class="{activate: currentItem === 2}">
          <text>
            毕业于四川大学华西口腔医学院，获口腔修复专业硕士学位，现任中华口腔医学会儿童口腔医学专业委员会专科会员、中华口腔医学会镇静镇痛专业委员会专科会员。曾就职于解放军306医院口腔科，从事口腔临床工作十余年。长儿童口腔疾病的治疗、早期矫治。
          </text>
        </view>
      </view>
    </swiper-item>
    <swiper-item>
      <view class="swiper-item">
        <view class="head">
          <img src="../../static/v2.1/expert-avatar-default.png" class="avatar"/>
          <text class="name">王英瑛</text>
        </view>
        <view class="card" :class="{activate: currentItem === 3}">
          <text>
            毕业于北京大学医学部，获口腔医学博士学位。曾就职于天津市口腔医院（暨南开大学口腔医院），赴美国内华达周立大学拉斯维加斯牙科学院交流访问。现就职于北京大学国际医院口腔科。曾获2017年全国口腔医学青年教师操作技能展示（牙体牙髓组）一等奖。现任中华口腔医学会牙体牙髓病学专委会会员、中华口腔医学会激光专委会会员。
          </text>
        </view>
      </view>
    </swiper-item>
    <swiper-item>
      <view class="swiper-item">
        <view class="head">
          <img src="../../static/v2.1/expert-avatar-default.png" class="avatar"/>
          <text class="name">郭力嘉</text>
        </view>
        <view class="card" :class="{activate: currentItem === 4}">
          <text>
            美国宾夕法尼亚大学牙学院博士后。主持和参加国家级及省部级课题9项。荣获北京口腔医学论坛优秀论文二等奖；荣获北京医学科技奖二等奖。北京口腔医学会口腔生物医学专委会青年委员。 中华口腔医学会正畸专业委员会（COS）会员，世界正畸联盟（WFO）国际会员，国际牙科研究会（IADR）国际会员，隐适美Invisalign官方认证医师。
          </text>
        </view>
      </view>
    </swiper-item>
    <swiper-item>
      <view class="swiper-item">
        <view class="head">
          <img src="../../static/v2.1/expert-avatar-default.png" class="avatar"/>
          <text class="name">马林</text>
        </view>
        <view class="card" :class="{activate: currentItem === 5}">
          <text>
            儿童牙科专业硕士研究生，协和医院无痛牙科治疗中心医师。2013年在奥地利维也纳大学接受国际口腔激光规范应用培训，2014年在美国德克萨斯健康医学中心、加州大学旧金山分校、TUFTS大学牙学院进行学术交流。 擅长各种成人和儿童牙体牙髓疾病的筛查治疗，尤其在儿童牙科恐惧症治疗方面有独到研究，开展了近千例不合作儿童的无痛舒适牙科治疗和镇静、麻醉治疗。
          </text>
        </view>
      </view>
    </swiper-item>
  </swiper>
  <!-- <uni-row class="demo-uni-row">
    <uni-col>
      <view class="demo-uni-col dark_deep">ee</view>
    </uni-col>
  </uni-row>

  <uni-row class="demo-uni-row">
    <uni-col :span="12">
      <view class="demo-uni-col dark">rr</view>
    </uni-col>
    <uni-col :span="12">
      <view class="demo-uni-col light">tt</view>
    </uni-col>
  </uni-row> -->

</template>

<script lang="ts">
  export default {
    name: "expert-card-v2",
    data() {
      return {
        currentItem: 0
      }
    },
    methods: {
      showSwiperItem(e: any) {
        this.currentItem = e.detail.current
      }
    }
  }
</script>

<style lang="scss" scoped>
  .swiper {
    height: 760rpx;
    width: 100%;
    // background: transparent !important;
    background-image: url("../../static/v2.1/swiper-bg.png");
    background-size: 100% 647rpx;
    background-repeat: no-repeat;
  }

  .swiper-item {
    width: 100%;
    height: 100%;
    background: transparent;
  }

  .head {
    display: flex;
    justify-content: flex-start;
    align-items: flex-end;
    padding: 0 30rpx 0 50rpx;
    box-sizing: border-box;
    margin-bottom: -70rpx;

    .avatar {
      width: 104rpx;
      height: 104rpx;
      border-radius: 50%;
      border: 4rpx #fff solid;
    }

    .name {
      font-size: 30rpx;
      font-weight: bold;
      color: #539F83;
      margin-left: 8rpx;
    }
  }

  .card {
    width: 500rpx;
    height: 550rpx;
    margin: 0 auto;
    padding: 90rpx 30rpx 20rpx;
    color: #333333;
    background-color: #A1CEBD;
    box-shadow: 2rpx 4rpx 11rpx 0 rgba(51, 51, 51, 0.19);
    border-radius: 25rpx;
    box-sizing: border-box;
    overflow: hidden;
    font-size: 24rpx;
  }
  .card.activate {
    background-color: #FFFFFF;
  }
</style>

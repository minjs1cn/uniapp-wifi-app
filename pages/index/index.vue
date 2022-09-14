<template>
  <view class="content">
    <image class="logo" src="/static/logo.png" />
    <view class="text-area">
      <text class="title">{{ title }}</text>
    </view>
    <view class="block">
      <uni-list>
        <uni-list-item v-for="item in list" :title="item.title" :show-badge="true" :badge-text="item.tel"
          :note="`密码: ${item.password}`"></uni-list-item>
      </uni-list>
    </view>
    <view class="text-area">
      <text class="title">更多店铺敬请期待</text>
    </view>
  </view>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const title = ref('店铺WIFI');
const list = ref([
  {
    title: '海兴路',
    password: 'haixinglu',
    tel: '0572-6320111'
  },
  {
    title: '明珠路',
    password: 'mingzhulu',
    tel: '0572-6320112'
  },
  {
    title: '长安路',
    password: 'changanlu',
    tel: '0572-6320113'
  },
  {
    title: '太湖路',
    password: 'taihulu',
    tel: '0572-6320114'
  },
  {
    title: '长洲路',
    password: 'changzhoulu',
    tel: '0572-6320115'
  },
]);
</script>

<style lang="scss">
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200rpx;
  width: 200rpx;
  margin-top: 50rpx;
  margin-left: auto;
  margin-right: auto;
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36rpx;
  color: $uni-text-color;
  margin: 40px auto;
}

.block {
  width: 100%;
}
</style>

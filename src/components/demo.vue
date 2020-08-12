<template>
  <div class="demo">
    <van-row class="data-list" gutter="20">
      <van-col span="8" v-for="(item,index) in dataList" :key="index" class="data-item">
        <div class="data-img">
          <img :src="item.img" alt />
        </div>
        <div class="data-name">
          <span>{{item.name}}</span>
        </div>
      </van-col>
    </van-row>
  </div>
</template>
 
<script>
export default {
  data() {
    return {
      dataList: [
        {
          img: require("../assets/image/jingdong.jpeg"),
          name: "百度",
        },
        {
          img: require("../assets/image/jingdong.jpeg"),
          name: "京东",
        },
        {
          img: require("../assets/image/jingdong.jpeg"),
          name: "贝壳",
        },
        {
          img: require("../assets/image/jingdong.jpeg"),
          name: "阿里",
        },
        {
          img: require("../assets/image/jingdong.jpeg"),
          name: "淘宝",
        },
      ],
    };
  },
};
</script>

<style scoped lang="less">
.demo {
  .data-list {
    padding: 0 1rem;
    .data-item {
      .data-img {
        margin-top: 2rem;
        height: 90px;
        img {
          object-fit: contain;
          width: 100%;
          max-height: 100%;
        }
      }

      .data-name {
        text-align: center;
        margin-top: 10px;
      }
    }
  }
}
</style>

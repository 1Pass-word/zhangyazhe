<template>
  <div>
    <div class="hezi">
      <h2>飙升榜</h2>
      <div class="lie" v-for="(item, index) in list" :key="index">
        <div class="left">
          <img :src="item.img" alt="" />
        </div>
        <div class="right">
          <p>{{ item.title }}</p>
          <span>{{ item.author }}</span>
        </div>
      </div>
      <button>查看全部</button>
    </div>
  </div>
</template>
<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      list: [
        {
          img: "https://bookcover.yuewen.com/qdbimg/349573/1033991975/90.webp",
          title: "1 资本的秘密",
          author: "林尔南多·德·家托",
        },
        {
          img: "https://bookcover.yuewen.com/qdbimg/349573/1037028803/90.webp",
          title: "2 快乐上等",
          author: "上野千鹤子 汤山玲子",
        },
        {
          img: "https://bookcover.yuewen.com/qdbimg/349573/1036497697/90.webp",
          title: "3 挣脱",
          author: "刘任侠",
        },
        {
          img: "https://bookcover.yuewen.com/qdbimg/349573/1037332517/90.webp",
          title: "4 法医秦明",
          author: "法医秦明",
        },
        {
          img: "https://bookcover.yuewen.com/qdbimg/349573/1033991975/90.webp",
          title: "5 宋词洗冤笔记",
          author: "巫童",
        },
        {
          img: "https://bookcover.yuewen.com/qdbimg/349573/1034479990/90.webp",
          title: "6 饮泓",
          author: "一枚铜钱",
        },
        {
          img: "https://bookcover.yuewen.com/qdbimg/349573/1037090668/90.webp",
          title: "7 金钱心理学",
          author: "摩根·豪泽尔",
        },
        {
          img: "https://bookcover.yuewen.com/qdbimg/349573/1037458244/90.webp",
          title: "8 三体",
          author: "刘慈欣",
        },
        {
          img: "https://bookcover.yuewen.com/qdbimg/349573/1037068783/90.webp",
          title: "9 活着",
          author: "余华",
        },
      ],
    };
  },
};
</script>
<style lang="less" scoped>
.hezi {
  .lie {
    display: flex;
    align-items: center;
    margin-top: 15px;
    .right {
      margin-left: 20px;
      span {
        font-size: 14px;
        color: #333;
        margin-left: 15px;
      }
      p {
        font-size: 18px;
      }
    }
  }
  button {
    width: 100%;
    height: 40px;
    margin-top: 15px;
    border: none;
    color: gray;
    font-size: 16px;
    border-radius: 10px;
  }
}
</style>

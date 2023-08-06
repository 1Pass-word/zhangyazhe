<template>
  <div>
    <div
      class="hezi"
      v-for="(item, index) in list"
      :key="index"
      @click="abb(index)"
    >
      <div class="left">
        <div class="left-1">
          <span>{{ item.id }}</span>
        </div>
        <div class="left-2">
          <img :src="item.img" alt="" />
        </div>
        <div class="left-3">
          <span>{{ item.name }}</span
          ><br />
          <a>{{ item.author }}</a>
          <p>{{ item.rate }}</p>
        </div>
      </div>
      <div class="right">
        <span>
          <svg
            t="1691066383444"
            class="icon"
            viewBox="0 0 1024 1024"
            version="1.1"
            xmlns="http://www.w3.org/2000/svg"
            p-id="4717"
            width="20"
            height="20"
          >
            <path
              d="M958.72 925.44c-15.36-181.76-139.52-332.16-307.84-386.56C721.28 493.44 768 414.72 768 324.48c0-141.44-115.2-256-256.64-256-141.44 0-256.64 114.56-256.64 256 0 90.24 46.72 168.96 117.12 214.4C204.16 593.28 79.36 743.68 64 925.44c0 3.2-0.64 5.76 0 10.24 1.28 16 15.36 28.8 31.36 28.8l831.36 0c16 0 30.08-12.8 31.36-28.8C959.36 931.2 958.72 928.64 958.72 925.44z"
              p-id="4718"
              fill="#c9c9c9"
            ></path>
          </svg>
          {{ item.renshu }}
        </span>
      </div>
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
          id: 1,
          img: "https://weread-1258476243.file.myqcloud.com/weread/cover/61/YueWen_822995/t6_YueWen_822995.jpg",
          name: "明朝那些事",
          author: "当年明月",
          rate: "推荐值92.4%",
          renshu: "5.0万",
        },
        {
          id: 2,
          img: "https://bookcover.yuewen.com/qdbimg/349573/1031737815/150.webp",
          name: "长安的荔枝",
          author: "马伯庸",
          rate: "推荐值95.5%",
          renshu: "1.4万",
        },
        {
          id: 3,
          img: "https://wfqqreader-1252317822.image.myqcloud.com/cover/844/34560844/t6_34560844.jpg",
          name: "中国史",
          author: "文伯灵",
          rate: "推荐值78.9%",
          renshu: "5893",
        },
        {
          id: 4,
          img: "https://wfqqreader-1252317822.image.myqcloud.com/cover/310/847310/t6_847310.jpg",
          name: "大明王朝",
          author: "刘和平",
          rate: "推荐值91.3%",
          renshu: "4563",
        },
        {
          id: 5,
          img: "https://bookcover.yuewen.com/qdbimg/349573/1031115172/150.webp",
          name: "弃长安",
          author: "张名扬",
          rate: "推荐值93.7%",
          renshu: "3009",
        },
        {
          id: 6,
          img: "https://bookcover.yuewen.com/qdbimg/349573/1036477734/150.webp",
          name: "三国争霸",
          author: "渤海小时",
          rate: "推荐值%90.0",
          renshu: "2909",
        },
        {
          id: 7,
          img: "https://weread-1258476243.file.myqcloud.com/weread/cover/37/YueWen_855812/t6_YueWen_855812.jpg",
          name: "人类简史",
          author: "尤瓦尔·赫拉利",
          rate: "推荐值87.8%",
          renshu: "2267",
        },
      ],
    };
  },
  methods: {
    abb(index) {
      if (this.list[index].id != 1 && this.list[index].id != 2) {
        this.list[index].renshu++;
      }
    },
  },
};
</script>
<style lang="less" scoped>
.hezi {
  margin-top: 20px;
  display: flex;
  justify-content: space-between;
  .left {
    width: 70%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    img {
      width: 90px;
      height: 120px;
    }
    .left-1 {
      span {
        font-size: 20px;
        font-weight: 600;
        color: #333;
      }
    }
    .left-3 {
      line-height: 30px;
      span {
        font-size: 18px;
        font-weight: 600;
      }
      a {
        font-size: 14px;
        font-weight: 400;
        color: #999;
      }
      p {
        font-size: 14px;
        font-weight: 400;
        color: #999;
      }
    }
  }
  .right {
    span {
      display: inline-block;
      background: #f6f6f6;
      width: 80px;
      height: 30px;
      text-align: center;
      line-height: 35px;
      border-radius: 50px;
    }
  }
}
</style>

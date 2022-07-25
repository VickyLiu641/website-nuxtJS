<template>
   <v-carousel
    cycle
    show-arrows-on-hover
    hide-delimiter-background
    delimiter-icon="mdi-minus"
  >
    <v-carousel-item
      v-for="(slide, i) in swiperList"
      :key="i"
      :src="slide.img"
    >
      <v-sheet
        color="rgba(0, 0, 0, 0.4)"
        height="100%"
        style="display: flex;align-items: center;justify-content: center;flex-wrap: wrap;"
      >
        <div >
          <h1 style="color:#fff;margin-bottom: 50px;font-size: 50px;">{{slide.title}}</h1>
          <h2 style="color:#fff;font-size: 20px;">{{slide.content}}</h2>
        </div>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
</template>
<script>

export default {
  name: "Banner",
  data() {
    return {
      swiperList: [
        {
          // img: require("@/assets/img/banner01.png"),
          img: "https://haha-front-end.oss-cn-hangzhou.aliyuncs.com/work-other/banner01-tuya.png",
          path: "",
          title: '为视光门店助力',
          content: '完善的视光门店系统，全方位服务！',
        },
        {
          img: "https://haha-front-end.oss-cn-hangzhou.aliyuncs.com/work-other/banner02-tuya.png",
          path: "",
          title: '学校视力筛查',
          content: '按照国家标准，快速进行视力筛查！',
        },
        // {
        //   img: require("@/assets/img/banner1.png"),
        //   path: "",
        //   title: '您身边的IT专家3',
        //   content: '宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介',
        // },
        // {
        //   img: require("@/assets/img/banner2.jpg"),
        //   path: "",
        //   title: '您身边的IT专家4',
        //   content: '宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介',
        // }
      ],
    };
  },
};
</script>

<style scoped lang="scss"></style>

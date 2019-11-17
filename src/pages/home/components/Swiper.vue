<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for=" item of swiperList " :key="item.id">
        <img
          class="swiper-img"
          :src="item.imgUrl"
        />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeSwiper",
  data() {
    return { 
      swiperOption: {
        pagination: ".swiper-pagination",
       loop:true,
      },
      swiperList:[{
          id:'001',
          imgUrl:'//source.qunarzz.com/site/images/wns/20191101_qunar_dujia_750x192_3.jpg'
      },{
          id:'002',
          imgUrl:'//source.qunarzz.com/site/images/wns/20191113_qunar_dujia_750x192_2.jpg'
      }],
    };
  }
};
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff;
}

.wrapper {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 27%;

  .swiper-img {
    width: 100%;
  }
}
</style>
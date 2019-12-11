<template>
<div>
    <div class="banner" @click="handleBannerClick">
        <img class="banner-img" src="https://img1.qunarzz.com/p/tts5/1703/a4/53de011d58a6302.jpg_r_640x420x90_712eae86.jpg" alt="">
        <div  class="banner-info" >
            <div class="banner-title">京都奈良自由行</div>
            <div class="banner-number">  <span class="iconfont banner-icon">&#xe692;</span>39</div>
        </div>
    </div>
    <CommonGallery :imgs="imgs" v-show="showGallery" @close="handleGalleryClose" ></CommonGallery>
    </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'

export default {
    name:'DetailBanner',
    data() {
        return {
            showGallery:false,
            imgs:['https://img1.qunarzz.com/p/tts5/1703/a4/53de011d58a6302.jpg_r_640x420x90_712eae86.jpg',
              'https://img1.qunarzz.com/vs_ceph_vs_tts/e83ca2d5-e2ab-43d2-8853-52fd76aefc7b.jpg_r_640x420x90_f8d84a8b.jpg']
        }
    },
    components:{
        CommonGallery,
    },
    methods:{
        handleBannerClick(){
            this.showGallery = true
        },
        handleGalleryClose(){
            this.showGallery = false
        }
    }
}
</script>

<style lang="stylus" scoped>
.banner 
    position :relative
    overflow: hidden
    height:0
    padding-bottom:55%
    .banner-img
        width :100%
    .banner-info
        display:flex;
        position:absolute;
        left:0
        right:0
        bottom:0
        line-height:.6rem
        color: #fff
        background-image: linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
        .banner-title
             flex:1
             font-size:0.32rem
             padding:0 0.2rem
        .banner-number
            padding:0 .4rem
            height: .32rem
            margin-top:0.14rem
            line-height:.32rem 
            border-radius:.2rem
            background:rgba(0,0,0,0.8)
            font-size:0.24rem
        .banner-icon
            font-size:0.24rem


</style>
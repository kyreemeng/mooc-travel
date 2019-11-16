<template>
    <div class="icons">
        <swiper >
            <swiper-slide v-for="(page,index) of pages" :key="index" >
            <div class="icon"
            v-for="item of page"
            :key="item.id"
            >
            <div class="icon-img">
                <img class="icon-img-content" :src="item.imgUrl" >
            </div>
            <p class="icon-desc">{{item.desc}}</p>
        </div>
        </swiper-slide>
      </swiper>
    </div>
</template>

<script>
export default {
    name: 'HomeIcons',
    data() {
        return {
            iconList:[{
            id:'001',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            desc:'景点门票'
            },{
            id:'002',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
            desc:'故宫'
            },{
            id:'003',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
            desc:'北京必游'
            },{
            id:'004',
            imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
            desc:'香山公园'
            },{
            id:'005',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
            desc:'一日游'
            },{
            id:'006',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/67/9a1678221b8e0e02.png',
            desc:'古水北镇'
            },{
            id:'007',
            imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/338c5b924c5809e8c7b14f60a953c3e2.png',
            desc:'欢乐谷'
            },{
            id:'008',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
            desc:'赏红叶'
            },{
            id:'009',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
            desc:'泡温泉'
            }]
        }
     
    },
    computed: {
         pages(){
            const pages=[]
            this.iconList.forEach((item,index)=>{
                const page = Math.floor(index/8)
                if (!pages[page]) {
                    pages[page]=[]
                }
                pages[page].push(item)
            })
            return pages
         }
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
.icons >>> .swiper-container
    height:0
    padding-bottom:50%
    .icon 
        position: relative
        overflow: hidden
        float :left
        width :25%
        height:0
        padding-bottom:25%
        .icon-img
            position:absolute
            top:0
            left:0
            right:0
            bottom:0.44rem
            box-sizing:border-box
            .icon-img-content
                display:block
                margin:0 auto
                height:100%
        .icon-desc
            position:absolute
            left:0
            right:0
            bottom:0
            height:0.44rem
            line-height:.44rem
            color:$darkTextColor
            text-align center
            ellipsis()



    
</style>
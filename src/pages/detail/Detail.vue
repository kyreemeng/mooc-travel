<template>
    <div>
        <DetailBanner></DetailBanner>
        <DetailHeader></DetailHeader>
        <div class="content" >
            <DetailList :list="list"></DetailList>
        </div>
    </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
export default {
    name:'Detail',
    components:{
        DetailBanner,
        DetailHeader,
        DetailList,
    },
    data() {
        return {
            list:[{
                title:'成人票',
                children:[{
                    title:'成人票场馆联票',
                     children:[{
                    title:'成人票场馆联票-红公馆',
                }]
                    
                },{
                    title:'成人票2'
                },{
                    title:'成人票3'
                },]
            },{
                title:'学生票'
            },{
                title:'儿童票'
            },{
                title:'特惠票'
            }]
        }
    },
}
</script>

<style lang="stylus" scoped>
.content
  height:20rem
</style>
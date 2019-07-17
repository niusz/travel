<template>

    <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</template>
<script>
export default {
    name: "HomeSwiper",
    data () {
        return {
            swiperOption: {
                pagination: '.swiper-pagination',
                loop: true
            },
            swiperList: [{
                id: '0001',
                imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/66f201b7c7702f9d2d51a1aed86b9f8f.jpg_750x200_179821e4.jpg'
            },{
                id: '0002',
                imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/4d35a34ee1637399d403704b18331d4d.jpg_750x200_2886cd69.jpg'
            }]
        }
    }
}
</script>
<style lang="stylus" scoped>
    >>> .swiper-pagination-bullet-active
        background: #fff !important
    .swiper-img 
        width: 100%
</style>
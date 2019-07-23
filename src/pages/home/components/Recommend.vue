<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <router-link
            tag="li" 
            class="item border-bottom"
             v-for="item of list" 
             :key="item.id"
             :to="'/detail/' + item.id">
                <img class="item-img" :src="item.imgUrl">
                <div class="item-info">
                    <p class="item-title">{{ item.title}}</p>
                    <p class="item-desc">{{ item.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </router-link>
        </ul>
    </div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
  // data (){
    //     return {
    //         recommendList: [{
    //         id: '0001',
    //         imgUrl: 'http://img1.qunarzz.com/sight/p0/1903/61/617ac4a711f6cb34a3.img.jpg_200x200_5e8ac1c0.jpg',
    //         title: '苏州乐园森林水世界苏州乐园森林水世界苏州乐园森林水世界苏州乐园森林水世界苏州乐园森林水世界',
    //         desc: ''
    //     },{
    //         id: '0002',
    //         imgUrl: 'http://img1.qunarzz.com/sight/p0/1903/61/617ac4a711f6cb34a3.img.jpg_200x200_5e8ac1c0.jpg',
    //         title: '苏州乐园森林水世界苏州乐园森林水世界苏州乐园森林水世界苏州乐园森林水世界苏州乐园森林水世界',
    //         desc: ''
    //     },{
    //         id: '0003',
    //         imgUrl: 'http://img1.qunarzz.com/sight/p0/1903/61/617ac4a711f6cb34a3.img.jpg_200x200_5e8ac1c0.jpg',
    //         title: '苏州乐园森林水世界苏州乐园森林水世界苏州乐园森林水世界苏州乐园森林水世界苏州乐园森林水世界',
    //         desc: ''
    //     }] 
    //     }
    // }
}
</script>
<style lang="stylus" scoped>
    @import '~styles/mixin.styl'
    .title 
        margin-top: .2rem
        line-height: .8rem
        background: #eee
        text-indent: .2rem
    .item
        overflow: hidden
        display: flex
        height: 1.9rem
        .item-img 
            width: 1.7rem
            height: 1.7rem
            padding: .1rem
        .item-info
            flex: 1
            padding: .1rem
            min-width: 0
            .item-title 
                line-height: .54rem
                font-size: .32rem
                ellipsis()
            .item-desc
                line-height: .54rem
                color: #ccc
                ellipsis()
            .item-button 
                line-height: .44rem
                margin-top: .2rem
                background: #ff9300
                padding: 0 .1rem 
                border-radius: .06rem

</style>
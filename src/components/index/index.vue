<template>
    <div class="index-box">
        <ul>
            <li v-for="(item,index) in cssFilterList" :key="index">
                <h4>{{item.title}}</h4>
                <div class="flex">
                    <div v-for="filters in item.list" :key="filters.cssfilter" class="flex filter-box">
                        <p>{{filters.name}}</p>
                        <div class="filter-item">
                            <h6>原图</h6>
                            <div>
                                <img :src="filters.url" alt="">
                            </div>
                        </div>
                        <div class="filter-item">
                            <div class="css">
                                {{filters.cssfilter}}
                            </div>
                            <div>
                                <img :src="filters.url" alt="" :style="filters.cssfilter">
                            </div>
                        </div>
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'index',
    data(){
        return {
            cssFilterList: [
                {
                    title: 'CSS filter 滤镜',
                    list: [
                        {
                            url: require('../../assets/img/1.jpg'),
                            cssfilter: 'filter: blur(5px);',
                            name: '滤镜-模糊'
                        },
                        {
                            url: require('../../assets/img/1.jpg'),
                            cssfilter: 'filter:brightness(1.4);',
                            name: '滤镜-亮度'
                        },
                        {
                            url: require('../../assets/img/1.jpg'),
                            cssfilter: 'filter:contrast(200%);',
                            name: '滤镜-对比度'
                        },
                        {
                            url: require('../../assets/img/1.jpg'),
                            cssfilter: 'filter:drop-shadow(4px 4px 8px blue);',
                            name: '滤镜-投影'
                        },
                        {
                            url: require('../../assets/img/1.jpg'),
                            cssfilter: 'filter:grayscale(50%);',
                            name: '滤镜-灰度'
                        },
                        {
                            url: require('../../assets/img/1.jpg'),
                            cssfilter: 'filter:hue-rotate(90deg);',
                            name: '滤镜-色调变化'
                        },
                        {
                            url: require('../../assets/img/1.jpg'),
                            cssfilter: 'filter:invert(75%);',
                            name: '滤镜-反相'
                        },
                        {
                            url: require('../../assets/img/1.jpg'),
                            cssfilter: 'filter:opacity(25%);',
                            name: '滤镜-透明度'
                        },
                        {
                            url: require('../../assets/img/1.jpg'),
                            cssfilter: 'filter:saturate(230%);',
                            name: '滤镜-饱和度'
                        },
                        {
                            url: require('../../assets/img/1.jpg'),
                            cssfilter: 'filter:sepia(60%);',
                            name: '滤镜-褐色'
                        }
                    ]
                }
            ]
        }
    }
}
</script>
<style scoped>
    li > h4{
        height: 40px;
        line-height: 40px;
        text-align: left;
        font-weight: bold;
        padding: 0 10px;
        border-bottom: 1px solid #999;
    }
    .filter-box{
        position: relative;
        padding-top: 30px;
        margin-top: 10px;
        border: 1px solid #ccc;
        border-radius: 5px;
        margin-right: 20px;
        padding: 40px 5px 5px 5px;
    }
    .filter-box > p{
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 30px;
        line-height: 30px;
        background-color: lightblue;
    }
    .filter-item{
        margin-right: 20px;
    }
    .filter-item:last-child{
        margin-right: 0;
    }
    .filter-item h6{
        height: 30px;
        line-height: 30px;
        color: #333;
    }
    .filter-item .css{
        width: 100%;
        height: 30px;
        line-height: 30px;
        background-color: rgba(43,43,43,0.2);
        color: #fff;
    }
</style>

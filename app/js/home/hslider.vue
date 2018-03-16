<template lang="html">
    
    <article>
        <slider :items="items" :cname="$style.slider"/>
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in lists":key=item.src>
                <router-link :to="{name:item.href}">
                    <img :src="item.src" alt="item.text">
                    <h4>{{item.text}}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>

<script>
import slider from './../core/slider.vue'
export default {
    components: {
        slider,
    },
    data() {
        return {
            items:[{
                href:"home",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t18766/238/863634487/49232/110e3799/5aaa4c59Ne1c04224.jpg?width=750&height=320",
            },{
                href:"home",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t17104/56/806488309/34011/59334e67/5aaa4cbbN76df4db7.jpg?width=750&height=320",
            },{
                href:"home",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t16420/311/2441901775/41509/ea55e221/5aaa4d09Nffaa582e.jpg?width=750&height=320",
            }],
            lists:[{
                href:"home",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
                text: "优惠券"
            },{
                href:"home",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
                text:"领红包",
            },{
                href:"home",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
                text:"抢钢镚",
            },{
                href:"home",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
                text:"白条提额",
            }]
        }
    }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.slider {
    margin-top:120px;
    img {
        width: 100%;
    }
}
.list {
    @include list(row);
    background: #fff;
    padding:40px 0 8px 0;
    margin-bottom: 20px;
    justify-content: space-around;
    a{
        text-decoration: none;
    }
    .item {
        text-align:center;
        img{
            display: inline-block;
            width: 90px;
            height: 90px;
        }
        h4 {
            margin-top:12px;
            font-size:26px;
            color:#666;
        }
        &:nth-child(3) h4{
            color:#f00
        }
    }
    

}
</style>

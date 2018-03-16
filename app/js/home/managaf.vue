<template lang="html">
    <Panel title="理财精选" :cname="$style.panel">
        <section :class="$style.content">
            <dl :class="$style.item">
                <dd>{{item.title}}</dd>
                <dt>{{item.rate}}</dt>
                <dt>{{item.text}}</dt>
            </dl>
        </section>
    </Panel>
</template>

<script>
import Panel from './../core/panel.vue'
export default {
    components: {
        Panel,
    },
    data() {
        return {
            items:[{
                title:"",
                sub:"",
                rate:"",
                text:"",
            },{
                title:"",
                sub:"",
                rate:"",
                text:"",
            },{
                title:"",
                sub:"",
                rate:"",
                text:"",
            },{
                title:"",
                sub:"",
                rate:"",
                text:"",
            }]
        }
    }
}
</script>

<style lang="scss">

</style>

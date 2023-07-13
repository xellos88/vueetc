<template>
    <div>
        <H1>PostComponent.vue</H1>
        <p>{{ propsTest }}</p>
    </div>
    <div>
        <slot></slot>
    </div>
</template>
<script>
import { ref,toRefs } from 'vue';
export default {
    name:'PostComponent',
    props: {
        propsTest:Number,
    },
    setup(props){
        let data= ref([]);
        let { propsTest } = toRefs(props);
        console.log(propsTest.value);
        
        return { data };
    }
}
</script>
<style>
    
</style>
<script setup>
import { computed } from 'vue'
import CrewmateSVG from './CrewmateSVG.vue';

const colors = ["#FF0000",  "#0000FF", "#00FFFF", "#C0C0C0", "#808080", "#800000", "#808000", "#00FF00", "#FF00FF", "#008000", "#FFFF00", "#800080", "#008080", "#000080"]
const props = defineProps({
    svgColorIndex: {
        type: Number,
        default: 0
    }
})
const svgColor = computed(() => colors[props.svgColorIndex])
const showKnife = computed(() => [7, 8, 10].includes(props.svgColorIndex))
</script>

<style>
.st0 {
    fill:#93CADF;
}

.st1 {
    fill: v-bind('svgColor')
}
</style>

<template>
    <div v-if="showKnife" v-mark="{ at: 1, color: 'red', type: 'circle' }" style="position: relative;">
        <img v-click="1" src="/among-us-knife.png" style="position: absolute; top: 0px; transform: rotate(45deg);"/>
        <!-- <img src="/among-us-knife.png" /> -->
        <CrewmateSVG />
    </div>
    <div v-else style="position: relative;">
        <img v-show="showKnife" v-click="1" src="/among-us-knife.png" style="position: absolute; top: 0px; transform: rotate(45deg);"/>
        <!-- <img src="/among-us-knife.png" /> -->
        <CrewmateSVG />
    </div>
</template>

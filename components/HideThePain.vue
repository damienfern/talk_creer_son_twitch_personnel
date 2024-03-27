<template>
    <div class="hidethepain-outerslot">
        <slot></slot>
        <img v-click="1" class="hidethepain" src="/hide-the-pain.png" alt=""/>
    </div>
</template>

<style>
.hidethepain-outerslot {
    position: relative;

    & > img.hidethepain {
        position: absolute;
        top: 0;
        left: 0; 
        margin-left: auto; 
        margin-right: auto; 
        width: 50px;
    }
}
</style>

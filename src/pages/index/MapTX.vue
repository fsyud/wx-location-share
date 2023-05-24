<template>
    <div id="container"></div>
</template>

<script setup lang="ts">
import { onMounted } from "vue";
const initMap = () => {
    //定义地图中心点坐标
    var center = new window.TMap.LatLng(39.98412, 116.307484);
    //定义map变量，调用 TMap.Map() 构造函数创建地图

    var map = new window.TMap.Map(document.getElementById("container"), {
        center: center, //设置地图中心点坐标
        zoom: 7.2, //设置地图缩放级别
        mapStyleId: "style1", //设置地图样式
    });
};
onMounted(() => {
    initMap();
});
</script>

<style>
#container {
    /*地图(容器)显示大小*/
    width: 100%;
    height: 100%;
}
</style>

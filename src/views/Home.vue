<template>
  <div class="outside-container">
    <baidu-map
      class="map"
      center="长春"
      :mapStyle="mapStyle"
      :zoom="1"
    ></baidu-map>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mapStyle: {
        styleJson: [
          {
            featureType: 'all',
            elementType: 'all',
            stylers: {
              lightness: 1,
              saturation: -100
            }
          },
          {
            featureType: 'land',
            elementType: 'all',
            stylers: {
              color: '#e2e1ddff'
            }
          },
          {
            featureType: 'water',
            elementType: 'all',
            stylers: {
              color: '#e2e1dd00'
            }
          }
        ]
      }
    }
  }
}
</script>

<style lang="less" scoped>
.outside-container {
  background: url(~@/assets/timg.jpg);
  width: 100%;
  height: 100%;
  .map {
    width: 100%;
    height: 100%;
  }
}
</style>

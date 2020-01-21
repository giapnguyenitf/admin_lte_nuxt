<template>
  <div class="info-box">
    <span :class="boxType" class="info-box-icon"
      ><i :class="ionClass" class="ion"></i
    ></span>

    <div class="info-box-content">
      <span class="info-box-text">{{ nameStatistic }}</span>
      <span class="info-box-number">{{ value }}<small>%</small></span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    boxType: {
      type: String,
      default: ''
    },
    nameStatistic: {
      type: String,
      default: ''
    },
    value: {
      type: Number,
      default: 0
    },
    ionClass: {
      type: String,
      default: ''
    }
  }
}
</script>

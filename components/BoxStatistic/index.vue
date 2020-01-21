<template>
  <div :class="boxType" class="small-box">
    <div class="inner">
      <h3>{{ value }}</h3>

      <p>{{ nameStatistic }}</p>
    </div>
    <div class="icon">
      <i :class="ionClass" class="ion"></i>
    </div>
    <a href="#" class="small-box-footer">
      More info
      <i class="fa fa-arrow-circle-right"></i>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: Number,
      default: 0
    },
    nameStatistic: {
      type: String,
      default: ''
    },
    boxType: {
      type: String,
      default: ''
    },
    ionClass: {
      type: String,
      default: ''
    }
  }
}
</script>

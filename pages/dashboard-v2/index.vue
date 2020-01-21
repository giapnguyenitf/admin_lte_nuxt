<template>
  <div>
    <breadcrumb
      :pageHeader="'Dashboard'"
      :optionalDescription="'Control panel'"
      :level="'Home'"
      :activeLevel="'Dashboard'"
    ></breadcrumb>
    <section class="content">
      <div class="row">
        <div class="col-lg-3 col-xs-6">
          <box-statistic
            :value="90"
            :nameStatistic="'CPU Traffic'"
            :boxType="'bg-aqua'"
            :ionClass="'ion-ios-gear-outline'"
          ></box-statistic>
        </div>
        <div class="col-lg-3 col-xs-6">
          <box-statistic
            :value="90"
            :nameStatistic="'Likes'"
            :boxType="'bg-red'"
            :ionClass="'ion-folder'"
          ></box-statistic>
        </div>
        <div class="col-lg-3 col-xs-6">
          <box-statistic
            :value="90"
            :nameStatistic="'Sales'"
            :boxType="'bg-green'"
            :ionClass="'ion-ios-cart-outline'"
          ></box-statistic>
        </div>
        <div class="col-lg-3 col-xs-6">
          <box-statistic
            :value="90"
            :nameStatistic="'New Members'"
            :boxType="'bg-yellow'"
            :ionClass="'ion-ios-people-outline'"
          ></box-statistic>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
import Breadcrumb from '~/layouts/Breadcrumb'
import BoxStatistic from '~/components/BoxStatistic/indexv2'

export default {
  layout: 'Master',
  components: {
    Breadcrumb,
    BoxStatistic
  }
}
</script>

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
            :value="100"
            :nameStatistic="'New Orders'"
            :boxType="'bg-aqua'"
            :ionClass="'ion-bag'"
          >
          </box-statistic>
        </div>
        <div class="col-lg-3 col-xs-6">
          <box-statistic
            :value="100"
            :nameStatistic="'Bounce Rate'"
            :boxType="'bg-green'"
            :ionClass="'ion-stats-bars'"
          >
          </box-statistic>
        </div>
        <div class="col-lg-3 col-xs-6">
          <box-statistic
            :value="100"
            :nameStatistic="'User Registrations'"
            :boxType="'bg-yellow'"
            :ionClass="'ion-person-add'"
          >
          </box-statistic>
        </div>
        <div class="col-lg-3 col-xs-6">
          <box-statistic
            :value="100"
            :nameStatistic="'Unique Visitors'"
            :boxType="'bg-red'"
            :ionClass="'ion-pie-graph'"
          >
          </box-statistic>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
import Breadcrumb from '~/layouts/Breadcrumb'
import BoxStatistic from '~/components/BoxStatistic/index'

export default {
  layout: 'Master',
  components: {
    Breadcrumb,
    BoxStatistic
  }
}
</script>

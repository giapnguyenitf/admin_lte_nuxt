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
            :typeBox="'bg-aqua'"
            :ionClass="'ion-bag'"
          >
          </box-statistic>
        </div>
        <div class="col-lg-3 col-xs-6">
          <box-statistic
            :value="100"
            :nameStatistic="'Bounce Rate'"
            :typeBox="'bg-green'"
            :ionClass="'ion-stats-bars'"
          >
          </box-statistic>
        </div>
        <div class="col-lg-3 col-xs-6">
          <box-statistic
            :value="100"
            :nameStatistic="'User Registrations'"
            :typeBox="'bg-yellow'"
            :ionClass="'ion-person-add'"
          >
          </box-statistic>
        </div>
        <div class="col-lg-3 col-xs-6">
          <box-statistic
            :value="100"
            :nameStatistic="'Unique Visitors'"
            :typeBox="'bg-red'"
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

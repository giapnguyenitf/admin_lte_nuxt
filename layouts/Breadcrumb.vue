<template>
  <section class="content-header">
    <h1>
      {{ pageHeader }}
      <small>{{ optionalDescription }}</small>
    </h1>
    <ol class="breadcrumb">
      <li>
        <a href="#"> <i class="fa fa-dashboard"></i> {{ level }} </a>
      </li>
      <li class="active">{{ activeLevel }}</li>
    </ol>
  </section>
</template>

<script>
export default {
  props: {
    pageHeader: {
      type: String,
      default: ''
    },
    optionalDescription: {
      type: String,
      default: ''
    },
    level: {
      type: String,
      default: ''
    },
    activeLevel: {
      type: String,
      default: ''
    }
  }
}
</script>

<template>
  <div class="wrapper">
    <header-page></header-page>
    <left-navbar></left-navbar>
    <app-main></app-main>
    <footer-page></footer-page>
  </div>
</template>
<script>
import HeaderPage from '~/layouts/HeaderPage'
import LeftNavbar from '~/layouts/LeftNavbar'
import FooterPage from '~/layouts/FooterPage'
import AppMain from '~/layouts/AppMain'

export default {
  name: 'Layout',
  components: {
    HeaderPage,
    LeftNavbar,
    AppMain,
    FooterPage
  }
}
</script>

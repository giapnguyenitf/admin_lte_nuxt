<template>
  <header class="main-header">
    <a href="" class="logo">
      <span class="logo-mini"><b>A</b>LT</span>
      <span class="logo-lg"> <b>Admin</b>LTE </span>
    </a>

    <nav class="navbar navbar-static-top" role="navigation">
      <a
        @click="toggleSideBarMenu()"
        href="#"
        class="sidebar-toggle"
        data-toggle="push-menu"
        role="button"
      >
        <span class="sr-only">Toggle navigation</span>
      </a>
      <div class="navbar-custom-menu">
        <ul class="nav navbar-nav">
          <dropdown-message></dropdown-message>
          <dropdown-notification></dropdown-notification>
          <dropdown-user></dropdown-user>
          <li>
            <a href="#" data-toggle="control-sidebar">
              <i class="fa fa-gears"></i>
            </a>
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script>
import DropdownNotification from '~/components/DropdownNotification/index'
import DropdownMessage from '~/components/DropdownMessage/index'
import DropdownUser from '~/components/DropdownUser/index'

export default {
  components: {
    DropdownNotification,
    DropdownMessage,
    DropdownUser
  },
  data() {
    return {
      toggleSideBar: false
    }
  },
  methods: {
    toggleSideBarMenu() {
      const body = document.body
      this.toggleSideBar
        ? body.classList.remove('sidebar-open')
        : body.classList.add('sidebar-open')
      this.toggleSideBar
        ? body.classList.remove('sidebar-collapse')
        : body.classList.add('sidebar-collapse')
      this.toggleSideBar = !this.toggleSideBar
    }
  }
}
</script>

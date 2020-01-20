<template>
  <li :class="{ open: showDropDown }" class="dropdown notifications-menu">
    <a ref="dropdownButton" @click="showDropDown = !showDropDown" href="#">
      <i class="fa fa-bell-o"></i>
      <span class="label label-warning">10</span>
    </a>
    <ul class="dropdown-menu">
      <li class="header">You have 10 notifications</li>
      <li>
        <ul class="menu">
          <li>
            <a href="#">
              <i class="fa fa-users text-aqua"></i> 5 new members joined today
            </a>
          </li>
          <li>
            <a href="#">
              <i class="fa fa-warning text-yellow"></i> Very long description
              here that may not fit into the page and may cause design problems
            </a>
          </li>
          <li>
            <a href="#">
              <i class="fa fa-users text-red"></i> 5 new members joined
            </a>
          </li>
          <li>
            <a href="#">
              <i class="fa fa-user text-red"></i> You changed your username
            </a>
          </li>
        </ul>
      </li>
      <li class="footer">
        <a href="#">View all</a>
      </li>
    </ul>
  </li>
</template>

<script>
export default {
  data() {
    return {
      showDropDown: false
    }
  },
  mounted() {
    document.addEventListener('click', this.documentClick)
  },
  destroyed() {
    document.removeEventListener('click', this.documentClick)
  },
  methods: {
    documentClick(e) {
      const el = this.$refs.dropdownButton
      const target = e.target
      if (el !== target && !el.contains(target)) {
        this.showDropDown = false
      }
    }
  }
}
</script>

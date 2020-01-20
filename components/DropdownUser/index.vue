<template>
  <li :class="{ open: showDropDown }" class="dropdown user user-menu">
    <a
      ref="dropdownButton"
      @click="showDropDown = !showDropDown"
      href="#"
      class="dropdown-toggle"
    >
      <img
        src="../../assets/img/avatar.png"
        class="user-image"
        alt="User Image"
      />
      <span class="hidden-xs">Alexander Pierce</span>
    </a>
    <ul class="dropdown-menu">
      <li class="user-header">
        <img
          src="../../assets/img/avatar.png"
          class="img-circle"
          alt="User Image"
        />

        <p>
          Alexander Pierce - Web Developer
          <small>Member since Nov. 2012</small>
        </p>
      </li>
      <li class="user-body">
        <div class="row">
          <div class="col-xs-4 text-center">
            <a href="#">Followers</a>
          </div>
          <div class="col-xs-4 text-center">
            <a href="#">Sales</a>
          </div>
          <div class="col-xs-4 text-center">
            <a href="#">Friends</a>
          </div>
        </div>
      </li>
      <li class="user-footer">
        <div class="pull-left">
          <a href="#" class="btn btn-default btn-flat">Profile</a>
        </div>
        <div class="pull-right">
          <a href="#" class="btn btn-default btn-flat">Sign out</a>
        </div>
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

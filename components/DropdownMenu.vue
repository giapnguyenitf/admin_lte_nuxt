<template>
  <li v-bind:class="{ 'menu-open': showDropDown }" class="treeview">
    <a @click.prevent="showDropDown = !showDropDown" href="#">
      <slot name="icon-menu"></slot>
      <span>{{ title }}</span>
      <span class="pull-right-container">
        <i class="fa fa-angle-left pull-right"></i>
      </span>
    </a>
    <ul v-show="showDropDown" class="treeview-menu">
      <slot name="dropdown-item"></slot>
    </ul>
  </li>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
      default: ''
    }
  },
  data() {
    return {
      showDropDown: false
    }
  },
  methods: {}
}
</script>

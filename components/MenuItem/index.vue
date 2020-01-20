<template>
  <li :class="{ active: isActive }" @click="isActive = !isActive">
    <router-link :to="path">
      <i :class="classIcon" class="fa"></i> <span>{{ title }}</span>
    </router-link>
  </li>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
      default: ''
    },
    classIcon: {
      type: String,
      required: true,
      default: ''
    },
    path: {
      type: String,
      required: true,
      default: '/'
    }
  },
  data() {
    return {
      isActive: false
    }
  }
}
</script>

<template>
  <div v-show="isActive">
    <!-- Tab item title will be inside the slot -->
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    name: { required: true },
    selected: { default: false }
  },

  data() {
    return {
      isActive: false
    }
  },
  mounted() {
    this.isActive = this.selected
  },

  created() {
    this.$parent.tabs.push(this)
  }
}
</script>

<style></style>

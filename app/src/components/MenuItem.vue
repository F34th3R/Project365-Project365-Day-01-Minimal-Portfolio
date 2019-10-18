<template>
  <div :class="[{ 'active': active}, 'menu-item']">
    <div class="menu-item-ico-container">
      <slot name="ico"></slot>
    </div>
    <h4>{{ title }}</h4>
    <div v-if="active" class="menu-item-active"></div>
  </div>
</template>

<script>
export default {
  name: 'MenuItem',
  props: {
    active: {
      type: Boolean,
      default: false
    },
    title: {
      type: String,
      required: true
    }
  }
}
</script>

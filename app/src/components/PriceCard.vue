<template>
  <div class="content-fotter-card">
    <span>
      {{ title }}
    </span>
    <h3>
      {{ ammount }}
    </h3>
    <div class="price">
      <div class="arrow">
        <img v-if="arrow" src="../assets/svg/green-arrow.svg">
        <img v-else src="../assets/svg/red-arrow.svg">
      </div>
      <span>{{ actualPrice }}</span>
    </div>
    <div class="price-progress"></div>
    <div class="price-progress-actual" :style="{ width: progress + 'px', 'background-color': background, }"></div>
  </div>
</template>

<script>
export default {
  name: 'PriceCard',
  props: {
    title: {
      type: String,
      required: true
    },
    ammount: {
      type: String,
      required: true
    },
    arrow: {
      type: Boolean,
      default: true
    },
    actualPrice: {
      type: String,
      default: '0'
    },
    progress: {
      type: String,
      default: '0'
    },
    background: {
      type: String,
      default: '#1B9BB0'
    }
  }
}
</script>

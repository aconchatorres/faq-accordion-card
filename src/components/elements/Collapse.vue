<template>
  <div class="collapse">
    <b-collapse
      class="card"
      animation="slide"
      v-for="(collapse, index) of collapses"
      :key="index"
      :open="isOpen == index"
      @open="isOpen = index"
    >
      <div
        slot="trigger"
        slot-scope="props"
        class="card-header"
        role="button">
        <p class="card-header-title" :style="props.open ? 'font-weight: bold !important;' : ''">
          {{ collapse.title }}
        </p>
        <a class="card-header-icon">
          <img v-if="props.open" class="up-arrow" src="../../assets/icons/icon-arrow-down.svg" alt="">
          <img v-else src="../../assets/icons/icon-arrow-down.svg" alt="">
        </a>
      </div>
      <div class="card-content">
        <p class="content">
          {{ collapse.text }}
        </p>
      </div>
    </b-collapse>
  </div>
</template>

<script>
export default {
  name: 'Collapse',
  props: {
    collapses: {
      type: Array,
      default: () => []
    },
    initial: {
      type: Number,
      default: 0
    }
  },
  data () {
    return {
      isOpen: 0
    }
  },
  created () {
    this.isOpen = this.initial
  }
}
</script>

<style lang="scss" scoped>
.card {
  padding: 5px 0;
  box-shadow: none !important;
  margin-top: 10px;
  border-bottom: 0.01em solid hsla(240, 6%, 50%, 0.404) !important;
  margin-right: 60px !important;
  @media screen and (max-width: 1024px) {
    margin-right: 0 !important;
  }
}
.card-header {
  box-shadow: none !important;
  margin-bottom: 8px !important;
}
.card-header-title {
  padding: 0 !important;
  font-weight: 100 !important;
}
.up-arrow {
  transform: rotate(180deg);
  -webkit-transform: rotate(180deg);
  -moz-transform: rotate(180deg);
  -o-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
}
.card-header-title:hover {
  color: hsl(14, 88%, 65%) !important;
}
.card-content {
  padding: 0 !important;
  padding-right: 24px !important;
  font-size: 14px;
  color: hsl(240, 6%, 50%);
  margin-bottom: 10px;
}
</style>

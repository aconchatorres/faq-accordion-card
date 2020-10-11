<template>
  <div class="FAQ">
    <div class="background-gradient">
      <div class="white-pill column is-half">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FAQ'
}
</script>

<style lang="scss" scoped>
.FAQ {
  .background-gradient {
    width: 100vw;
    height: 100vh;
    background-image: linear-gradient(hsl(273, 75%, 66%), hsl(240, 73%, 65%));
    display: table-cell;
    vertical-align: middle;
  }
  .white-pill {
    width: 63vw;
    height: 65vh;
    background-color: white;
    margin: auto;
    border-radius: 25px;
  }
}
</style>

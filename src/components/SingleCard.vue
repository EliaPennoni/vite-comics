<script>
export default {
  props: {
    product: Object,
  },
};
</script>

<template>
    <div class="comics">
      <img :src="product.thumb" alt="" />
      <h6>{{ product.series }}</h6>
    </div>
</template>

<style lang="scss"scoped>

.comics {
  width: calc((100% / 6) - 15px);
  margin-right: 15px;
  margin-bottom: 15px;
  img {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }
  h6{
    color: white;
    margin-top: 15px;
  }
}
</style>
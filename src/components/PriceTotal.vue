<template>
  <div class="shipping-total">
    <h1>{{ name }}</h1>
    <p>{{ price }}</p>
  </div>
</template>

<script>
export default {
  name: 'PriceTotal',
  props: {
    name: {
      type: String,
      default: null,
    },
    price: {
      type: String,
      default: null,
    }
  }
}
</script>

<style scoped>
  .price-total {
    width: 100%;
  }

  .price-total .shipping-total {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    border-top: 1px solid var(--gray-300);
    padding-top: 10.73px;
  }

  .price-total .shipping-total h1 {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 18px;
    line-height: 22px;
    color: var(--gray-900);
  }

  .price-total .shipping-total p {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 14px;
    line-height: 17px;
    color: var(--gray-900);
  }

  @media(max-width: 850px) {
    .price-total .shipping-total h1 {
      font-size: 14px;
      line-height: 17px;
    }

    .price-total .shipping-total p {
      font-size: 14px;
      line-height: 17px;
    }
  }
</style>
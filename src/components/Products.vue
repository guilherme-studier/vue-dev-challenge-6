<template>
  <div class="product">
    <Product name="Vintage Backbag" promo="R$54.99" price="R$94.99" :photo="photo1" />
    <Product name="Levi Shoes" promo="R$74.99" price="R$124.99" :photo="photo2" />
    <div class="price-total">
      <PriceTotal name="Shipping" price="$19" />
      <PriceTotal name="Total" price="$148.98" />
    </div>
  </div>
</template>

<script>
import Product from './Product.vue';
import PriceTotal from './PriceTotal.vue';

import photo1 from '../assets/photo1.png';
import photo2 from '../assets/photo2.png';

export default {
  name: 'Products',
  components: {
    Product,
    PriceTotal,
  },
  data() {
    return {
      photo1: photo1,
      photo2: photo2,
    }
  }
}
</script>

<style scoped>
  .product {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 319.57px;
    padding: 33.41px 0 20px 0;
  }

  .product .price-total {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 87.73px;
  }

  .product .price-total .shipping-total {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    border-top: 1px solid var(--gray-300);
    padding-top: 10.73px;
  }

  .product .price-total .shipping-total h1 {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 18px;
    line-height: 22px;
    color: var(--gray-900);
  }

  .product .price-total .shipping-total p {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 14px;
    line-height: 17px;
    color: var(--gray-900);
  }
</style>
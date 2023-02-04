<template>
<section>
  <div class="product-img">
    <img :src="photo" alt="">
  </div>
  <div class="product-value">
    <h3>{{ name }}</h3>
    <div class="price">
      <h4 class="price-promo">{{ promo }}</h4>
      <p class="price-real">{{ price }}</p>
    </div>
    <div class="count">
      <span @click="count--">-</span>
      <p>{{ count }}</p>
      <span @click="count++">+</span>
      </div>
  </div>
</section>
</template>

<script>
export default {
  name: 'Product',
  props: {
    name: {
      type: String,
      default: null
    },
    promo: {
      type: String,
      default: null
    },
    price: {
      type: String,
      default: null
    },
    photo: {
      type: String,
      default: null
    }
  },
  data() {
    return {
      count: 1,
    }
  },
}
</script>

<style scoped>
  section {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }

  .product-img {
    width: 134.21px;
    height: 136.27px;
    margin-right: 20.19px;
  }

  .product-img img {
    width: 100%;
    border-radius: 13px;
  }

  .product-value {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    text-align: initial;
  }

  .product-value h3 {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 20px;
    color: var(--gray-700);
  }

  .product-value .price {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
  }

  .product-value .price .price-promo {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 20px;
    color: var(--orange-500);
    margin-right: 10px;
  }

  .product-value .price .price-real {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 12px;
    line-height: 15px;
    text-decoration-line: line-through;
    color: var(--gray-700);
  }

  .product-value .count {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    border: 1px solid var(--gray-600);
    border-radius: 12px;
    padding: 15px 13px;
  }

   .product-value .count p {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 20px;
    color: var(--gray-900);
   }

   .product-value .count span {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 20px;
    color: var(--gray-900);

    font-size: 23px;
    color: #828282;
    background: #e0e0e0;
    padding: 2px 8px;
    border-radius: 4px;
    cursor: pointer;
   }

   @media(max-width: 850px) {
    .product-img {
      width: 122.75px;
      height: 124.64px;
      margin-right: 18.47px;
    }

    .product-value h3 {
      font-size: 12px;
      line-height: 15px;
    }

    .product-value .price .price-promo {
      font-size: 14px;
      line-height: 17px;
    }

    .product-value .price .price-real {
      font-size: 12px;
      line-height: 15px;
    }

    .product-value .count {
      padding: 15px 10px;
    }
  }
</style>
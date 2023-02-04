<template>
  <header>
    <h1>Checkout</h1>
  </header>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style scoped>
  header h1 {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 36px;
    line-height: 44px;
    color: var(--gray-700);
    text-align: initial;
    margin-top: 52px;
    margin-bottom: 50.94px;
    text-align: initial;
  }

  @media(max-width: 850px) {
    header h1 {
      font-size: 24px;
      line-height: 29px;
      margin-top: 32px;
      margin-bottom: 20.96px;
    }
  }
</style>
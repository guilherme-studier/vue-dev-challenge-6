<template>
  <section>
    <div class="form">
      <div class="contact-information">
        <h2>Contact information</h2>
        <Input label="E-mail" type="email" placeholder="Enter your email..." />
        <Input label="Phone" type="number" placeholder="Enter your phone..." />
      </div>
      <div class="shipping">
        <h2>Shipping address</h2>
        <Input label="Full name" type="text" placeholder="Your name..." value="Rodney Cotton" />
        <Input label="Address" type="text" placeholder="Your address..." />
        <Input label="City" type="text" placeholder="Your city..." />
        <div class="shipping-addres">
          <Select label="Country" placeholder="Your country..." />
          <Input label="Postal code" type="text" placeholder="Your postal code..." />
        </div>
      </div>
      <div class="check-box">
        <input type="checkbox">
        <p>Save this information for next time</p>
      </div>
      <div class="button">
        <button>Continue</button>
      </div>
    </div>
    <div class="shopping">
      <Products />
    </div>
  </section>
  <Footer />
</template>

<script>
import Input from './Input.vue';
import Select from './Select.vue';
import Products from './Products.vue';
import Footer from './Footer.vue';

export default {
  name: 'Formulários',
  components: {
    Input,
    Select,
    Products,
    Footer
  }
}
</script>

<style scoped>
  section {
    max-width: 960px;
    width: 100%;

    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-bottom: 159px;
  }

  section .form {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    max-width: 465px;
    width: 100%;

    height: 786.86px;
  }

  section .form .contact-information {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    
    height: 212.93px;
  }

  section .form .contact-information h2 {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 18px;
    line-height: 22px;
    color: var(--gray-900);
    text-align: initial;
  }

  section .form .shipping {
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    height: 394.95px;
  }

  section .form .shipping h2 {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 18px;
    line-height: 22px;
    color: var(--gray-900);
    text-align: initial;
  }

  section .form .shipping select {
    text-decoration: none;
    padding: 0;
    padding: 18px 14px;
    border-radius: 12px;
    border: 1px solid var(--gray-600);

    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 20px;
    color: var(--gray-800);
  }

  section .form .shipping .shipping-addres {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  section .form .shipping .shipping-addres div {
    max-width: 217px;
  }

  section .form .shipping .shipping-addres div:first-child {
    margin-right: 23.28px;
  }

  section .check-box {
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  section .check-box input {
    width: 21px;
    height: 21px;
    margin-right: 11px; 
  }

  section .check-box p {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 12px;
    line-height: 15px;
    color: var(--gray-800);
  }

  section .shopping {
    display: flex;
    justify-content: center;
    background: var(--gray-400);
    border-radius: 12px;

    width: 383px;
    max-height: 535px;
  }

  section .form .button {
    display: flex;
    justify-content: end;
  }

  section .button button {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 20px;
    background: var(--orange-500);
    padding: 17px 45px;
    border-radius: 12px;
    border: none;
    color: var(--white);
    cursor: pointer;

    transition: 0.2s;
  }

  section .button button:hover {
    color: var(--orange-500);
    background: var(--white);
    border: 1px solid var(--orange-500);
  }

  @media(max-width: 850px) {
    section {
      flex-direction: column-reverse;
      margin-bottom: 94.98px;
    }

    section .form {
      margin: 39px 0 20.49px 0;
      height: 605.1px;
    }

    section .shopping {
      width: 100%;
      height: 489px;
      max-width: 350px;
    }

    section .form .contact-information {
      height: 158.42px;
    }

    section .form .contact-information h2 {
      font-size: 14px;
      line-height: 17px;
    }

    section .form .shipping {
      height: 295.13px;
    }

    section .form .shipping h2 {
      font-size: 14px;
      line-height: 17px;
    }

    section .check-box input {
      margin-right: 7.78px; 
    }
  }

</style>
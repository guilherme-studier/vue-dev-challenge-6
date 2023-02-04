<template>
  <div class="input">
    <label>{{ label }}</label>
    <select :placeholder="placeholder">
      <option value="Canoas">Canoas</option>
      <option value="Porto Alegre">Porto Alegre</option>
      <option value="Caxias">Caxias</option>
    </select>
  </div>
</template>

<script>
export default {
  name: 'Select',
  props: {
    label: {
      type: String,
      default: null,
    },
    placeholder: {
      type: String,
      default: null,
    },
  }
}
</script>

<style scoped>
  .input {
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    height: 77.97px;
    width: 100%;
    min-width: 162.98px;
  }
  label {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 600;
    font-size: 12px;
    line-height: 15px;
    text-align: initial;
    color: var(--gray-800);
  }

  select {
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
    height: 56px;
    color: var(--gray-800);
  }

  @media(max-width: 850px) {
    .input {
      height: 57.06px;
    }

    label {
      font-size: 10px;
      line-height: 12px;
    }

    select {
      font-size: 12px;
      line-height: 15px;
      height: 40.56px;
    }
  }
</style>
<template>
  <div class="htmlClass">
    <h1>{{ title }}</h1>
    <form>
      <input type="text" id="firstName" v-model="firstName" />
      <input type="text" id="secondName" v-model="secondName" />
      <input type="text" id="nickname" v-model="nickname" />
      <input type="text" id="studentcode" v-model="studentcode" />
      <button @click="submitForm()" class="submitForm">Submit</button>
  </form>
  </div>
</template>

<script>
export default {
  name: 'InputPage',
  data() {
    return {
      title: 'Input Page.',
      firstName: 'Pakon',
      secondName: 'Rakmai',
      nickname: 'TOTO',
      studentcode: '6604101364',
    }
  },
  methods: {
    submitForm() {
      this.$emit('submit form')
    },
  }
}
</script>

<style scoped>

  h1 {
    text-align: center;
  }

  form {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: white;
    padding: 20px;
    border-radius: 10px;
  }

  input[type="text"] {
    width: 100%;
    max-width: 300px;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 16px;
  }

  button.submitForm {
    width: 100%;
    max-width: 300px;
    padding: 10px;
    margin-top: 20px;
    background-color: #00a6e7;
    color: white;
    border: none;
    border-radius: 5px;
    font-size: 18px;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }

  button.submitForm:hover {
    background-color: #008ac0;
  }

  button.submitForm:active {
    background-color: #006f9b;
  }

</style>

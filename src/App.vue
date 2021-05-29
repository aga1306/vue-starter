<template>
  <div>
    <h1>Witaj w systemie do zapisow na zajecia</h1>
   <div v-if="authenticatedEmail != '' ">
    <h4> Witaj {{ email }}</h4>
    <a @click="logMeOut()">Wyloguj</a>
    </div >
    <div v-else>
    Zaloguj sie emailem
    <input type="text" v-model="email">
    <button @click="logMeIn()">Wchodze</button>
      </div>
  </div>
</template>

<script>
export default {
  data() {
  return {
    email: 'aga@mail.pl',
    authenticatedEmail: ''
  };
},
  methods: {
  logMeIn() {
    this.authenticatedEmail = this.email;
  },
  logMeOut() {
    this.authenticatedEmail = '';
    this.email = '';
  }
}
};
</script>

<style>

</style>

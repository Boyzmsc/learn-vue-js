<template>
  <form action="">
    <div>
      <label for="username">id: </label>
      <input id="username" type="text" v-model="username">
    </div>
    <div>
      <label for="password">pw: </label>
      <input id="password" type="password" v-model="password">
    </div>
    <button v->login</button>
  </form>
</template>

<script>
export default {
  data: function(){
    return {
      username : '',
      password : ''
    }
  },
  methods: {

  }
}
</script>

<style>

</style>
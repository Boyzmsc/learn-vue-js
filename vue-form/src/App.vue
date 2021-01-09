<template>
  <form v-on:submit="submitForm">
    <div>
      <label for="username">id: </label>
      <input id="username" type="text" v-model="username">
    </div>
    <div>
      <label for="password">pw: </label>
      <input id="password" type="password" v-model="password">
    </div>
    <button type="submit">login</button>
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
    submitForm : function(event){
      // submit의 새로고침 기능 방지
      event.preventDefault();
      console.log(this.username, this.password);
    }
  }
}
</script>

<style>

</style>
<template>
  <form v-on:submit.prevent="submitForm">
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
// axios를 사용하기 위한 import
import axios from 'axios';

export default {
  data: function(){
    return {
      username : '',
      password : ''
    }
  },
  methods: {
    submitForm : function(){
      // submit의 새로고침 기능 방지
      // event.preventDefault() (or) submit.prevent = "submitForm"
      console.log(this.username, this.password);
      // 서버에 post로 전송 using axios
      var url = "https://jsonplaceholder.typicode.com/users";
      var data = {
        username : this.username,
        password : this.password
      }
      axios.post(url, data)
        .then(function(response){
          console.log(response);
        })
        .catch(function(error){
          console.log(error);
        });
    }
  }
}
</script>

<style>

</style>
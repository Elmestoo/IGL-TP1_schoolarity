<template>
  <div id="app">
    <login></login>
  </div>
</template>

<script>
import login from './components/login.vue';
export default {
  data : function(){
    return
  },
  components:{login}
}
</script>

<style>

#app {
  text-align:center;
}
body{
    text-align:center;
    background-color: #77aa77;
    background-image: url(file:///home/mestoo/Downloads/Abstract-Envelope.svg);
    background-attachment: fixed;
    background-size: cover;

}
</style>

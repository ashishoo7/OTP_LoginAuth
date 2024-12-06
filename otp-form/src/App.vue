<template>

  <body>
   <card>
   </card>
   <GetOtp>
  </GetOtp>
  <div>
  </div>
  </body>
</template>

<script>
import card from './components/card.vue';
import GetOtp from './components/GetOtp.vue';
export default{
  name:'App',
  components: {
    card,
    GetOtp,
  }
}
</script>
<style>
body {
  background-color: #3490DC;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}
</style>

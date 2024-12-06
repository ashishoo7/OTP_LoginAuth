<template>
     <div class="login-box">
      <!-- Company Logo -->
      <div class="logo">
        <img src="C:\Users\kalpa\OneDrive\Desktop\FirstVue\first-app\src\assets\logo.png" alt="Company Logo" />
      </div>
      </div>
      
</template>

<script>

export default {
  name: "card",
  
}

</script>

<style scoped>
/* Centered Box */
.login-box {
  justify-content: center;
  background-color: #fff;
  width: vw;
  height:vh;
  padding: 100px;
  border-radius: 8px;
  text-align: center;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

/* Logo */
.logo img {
  max-width: 100%;
  height: auto;
  margin-bottom: 20px;
}
</style>
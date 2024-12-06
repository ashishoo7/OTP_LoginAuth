<template>
    
      <!-- Input Box -->
      <input 
        type="text" 
        placeholder="Enter registered mobile number or email" 
        class="input-box"
      />
      <!-- Button -->
        <div><button class="login-button" @click="getOtp">GET OTP</button></div>
        <!-- Footer Links -->
        <div class="footer-links">
          <p>
          <a href="#" class="link">LOGIN USING PASSWORD</a>
        </p>
        <p>
          <a href="#" class="link">FORGOT PASSWORD</a>
        </p>
      </div>
 
</template>

<script>
import axios from "axios";

export default {
  name: "GetOtp",
  data() {
    return {
      userInput: "", // Holds the mobile number or email entered by the user
    };
  },
  methods: {
    async getOtp() {
      if (!this.userInput) {
        // alert("Please enter your registered mobile number or email.");
        // return;
      }

      try {
        const response = await axios.post("https://your-api-endpoint.com/get-otp", {
          input: this.userInput,
        });

        if (response.data.success) {
          alert("OTP sent successfully!");
        } else {
          alert(response.data.message || "Failed to send OTP. Please try again.");
        }
      } catch (error) {
        console.error("Error sending OTP:", error);
        alert("An error occurred while sending OTP. Please try again later.");
      }
    },
  },
};
</script>

<!-- <style scoped>
/* Input Box */
.input-box {
  
  width: 70%;
  padding: 10px;
  margin: 10px 0;
  border: 1px solid #ccc;
  border-radius: 4px;
  font-size: 14px;
}

/* Submit Button */
.login-button {
  background-color: #3490DC;
  color: white;
  border: none;
  padding: 10px;
  width: 20%;
  font-size: 14px;
  cursor: pointer;
  border-radius: 4px;
}

.login-button:hover {
  background-color: #2779bd;
}

/* Footer Links */
.footer-links {
  text-align: left;
  margin-top: 20px;
}

.footer-links .link {
  color: #3490DC;
  font-size: 12px;
  text-decoration: none;
}

.footer-links .link:hover {
  text-decoration: underline;
}
</style> -->

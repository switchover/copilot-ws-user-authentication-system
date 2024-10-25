<template>
  <div class="register">
    <h1>Register</h1>
    <form @submit.prevent="register">
      <div>
        <label for="name">Name:</label>
        <input type="text" v-model="name" required />
      </div>
      <div>
        <label for="email">Email:</label>
        <input type="email" v-model="email" required />
      </div>
      <div>
        <label for="phoneNumber">Phone Number:</label>
        <input type="text" v-model="phoneNumber" required />
      </div>
      <div>
        <label for="storeCode">Store Code:</label>
        <input type="text" v-model="storeCode" required />
      </div>
      <div>
        <label for="password">Password:</label>
        <input type="password" v-model="password" required />
      </div>
      <button type="submit">Register</button>
    </form>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      name: '',
      email: '',
      phoneNumber: '',
      storeCode: '',
      password: ''
    };
  },
  methods: {
    async register() {
      try {
        const response = await axios.post('/api/users/register', {
          name: this.name,
          email: this.email,
          phoneNumber: this.phoneNumber,
          storeCode: this.storeCode,
          password: this.password
        });
        console.log('User registered:', response.data);
      } catch (error) {
        console.error('Error registering user:', error);
      }
    }
  }
};
</script>

<style scoped>
.register {
  max-width: 400px;
  margin: 0 auto;
}
</style>

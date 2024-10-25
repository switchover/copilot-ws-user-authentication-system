<template>
  <div class="user-info">
    <h1>User Information</h1>
    <form @submit.prevent="updateUser">
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
        <input type="password" v-model="password" />
      </div>
      <button type="submit">Update</button>
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
    async updateUser() {
      try {
        const response = await axios.put('/api/users/update', {
          name: this.name,
          email: this.email,
          phoneNumber: this.phoneNumber,
          storeCode: this.storeCode,
          password: this.password
        });
        console.log('User updated:', response.data);
      } catch (error) {
        console.error('Error updating user:', error);
      }
    }
  }
};
</script>

<style scoped>
.user-info {
  max-width: 400px;
  margin: 0 auto;
}
</style>

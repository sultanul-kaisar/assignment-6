<script>
import { ref } from 'vue';
export default {
  setup() {
    const username = ref('');
    const password = ref('');

    const login = () => {
      // Perform validation and login logic here
      // Check if the username and password match the stored information
      // Redirect the user to the welcome page upon successful login
    };

    return {
      username,
      password,
      login
    };
  }
};
</script>


<template>
  <div class="container mx-auto">
    <h1 class="text-2xl font-bold mb-4">Login</h1>
    <form @submit.prevent="login">
      <div class="mb-4">
        <label for="username" class="block mb-2">Username</label>
        <input type="text" id="username" v-model="username" class="border border-gray-300 px-4 py-2 rounded w-full">
      </div>
      <div class="mb-4">
        <label for="password" class="block mb-2">Password</label>
        <input type="password" id="password" v-model="password" class="border border-gray-300 px-4 py-2 rounded w-full">
      </div>
      <button type="submit" class="bg-blue-500 text-white px-4 py-2 rounded">Login</button>
    </form>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>

<template>
  <div>
    <h1>Register</h1>

    <input
      type="email"
      name="email"
      placeholder="your email"
      v-model="email"
    >
    <input
      type="password"
      name="password"
      placeholder="password"
      v-model="password"
    >
    <button>register</button>
  </div>
</template>

<script>
import AuthenticationService from '@/services/AuthenticationService'

export default {
  data () {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    async register () {
      await AuthenticationService.register({
        email: this.email,
        password: this.password
      })
    }
  }
}
</script>

<style scoped>

</style>

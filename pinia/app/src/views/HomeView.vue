<template>
  <div>
    <h1>Login</h1>
    <button @click="login">Log me in</button>
  </div>
</template>

<script setup>
import { useRouter } from 'vue-router'
import { useAuthStore } from '@/stores/auth'

const router = useRouter()
const auth = useAuthStore()

function login() {
  auth.login()
  router.push('/about')
}
</script>

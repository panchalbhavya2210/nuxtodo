<script setup lang="ts">
//@ts-ignore
const route = useRoute()

const supbase = useSupabaseClient();

/**
 * * this is a function of signup


// const handleSignUp = async () => {
//   try {
//     const { error } = await supbase.auth.signUp({ email: emailVal, password: passwordVal })
//     console.log(error)
//   }
//   catch {

//   }
// }
 */

// let emailVal = "panchalbhavya2210@gmail.com"
// let passwordVal = "123456"

// const handleLogin = async () => {
//   try {
//     const { error } = await supbase.auth.signInWithPassword({ email: emailVal, password: passwordVal })
//   }
//   catch {

//   }

// }

// handleLogin()


const res = await supbase.auth.getUser()
//@ts-ignore
const uid = res.data.user.id
console.log(res)
console.log(uid)
</script>

<template>
  <div class="todoRender">
    hello from index
  </div>
</template>

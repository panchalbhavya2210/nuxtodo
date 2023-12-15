<script setup lang="ts">
//@ts-ignore
const route = useRoute()

const supbase = useSupabaseClient();

let emailVal = "panchalbhavya2210@gmail.com"
let passwordVal = "123456"

const handleSignUp = async () => {
  try {
    const { error } = await supbase.auth.signUp({ email: emailVal, password: passwordVal })
    console.log(error)
  }
  catch {

  }
}
</script>

<template>
  <div class="todoRender">

  </div>
</template>

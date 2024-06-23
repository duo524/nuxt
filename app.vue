<template>
  <div>
    <NuxtRouteAnnouncer />
    <NuxtWelcome />
  </div>
</template>


<script setup lang="ts">
const email = useState(() => '')
const onLogin = () => {
  $fetch('/api/login', {
    method: 'post',
    body: {
      email: 'r1575976602@163.com',
    },
  }).then((user) => {
    console.log(user)
  }).catch((err) => {
    console.log(err)
  })
}
onLogin()
</script>

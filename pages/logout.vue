<template>
  <div class="">

  </div>
</template>

<script>
export default {
  name: 'LogoutPage',
  head:{
    title: "Logout - Asthar Bazar - Promises 100% Reliance"
  },
  mounted() {
    localStorage.removeItem('token')
    this.$router.push('/')
  }
}
</script>

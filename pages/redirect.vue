<template>
  <div class='h-screen flex justify-center items-center'>
    Please Wait...
  </div>
</template>

<script>
export default {
  name: 'redirect',
  mounted() {
    try{
      const authorization = this.$route.query['authorization']
      if (!authorization) this.$router.push('/login')

      const token = JSON.parse(authorization)
      if (!token) this.$router.push('/login')

      localStorage.setItem('authorization', authorization)
      this.$router.push('/')
    } catch (e) {
      this.$router.push('login')
    }
  }
}
</script>

<style scoped>

</style>

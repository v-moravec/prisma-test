<template>
  <div>
    <div class="bg-red-50 w-fit" @click="createUser">
      CREATE USER
    </div>
    <div v-for="user in users" :key="user.id">
      {{ user }}
    </div>
  </div>
</template>

<script lang="ts" setup>

const { data: users } = await useFetch('/api/users')

async function createUser () {
  console.log(await useFetch('/api/create-user'))
}

</script>

<style lang="scss" scoped>

</style>

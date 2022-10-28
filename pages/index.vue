<template>
  <section class="container">
    <!-- <p class="title">{{ message }}</p>
    <hr />
    <ul>
      <li>
        <router-link to="/price">Price Page</router-link>
      </li>
      <li>
        <router-link to="/mypage">My Page</router-link>
      </li>
      <li>
        <router-link to="/users">users/index</router-link>
      </li>
      <li>
        <router-link to="/users/other">users/other</router-link>
      </li>
    </ul> -->
    <div>{{ users }}</div>
  </section>
</template>

<script>

const axios = require('axios')
let url = 'https://jsonplaceholder.typicode.com/users'

export default {
  asyncData({ params }) {
    return axios.get(url)
      .then((res) => {
        return { users: res.data }
      })
  }
}

</script>

<style scoped>
.title {
  font-family: "M PLUS Rounded 1c";
}
</style>

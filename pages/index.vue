<template>
  <section class="container">
    <p>{{ message }}</p>
    <hr />
    <ul>
      <li>
        <router-link to="/price">Price Page</router-link>
      </li>
      <li>
        <router-link to="/mypage">My Page</router-link>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data: function() {
    return {
      message: 'Hello World!'
    }
  }
}
</script>

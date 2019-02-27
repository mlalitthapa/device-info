<template>
  <nav class="uk-navbar-container" uk-navbar>
    <div class="uk-navbar-left">
      <ul class="uk-navbar-nav">
        <li>
          <nuxt-link to="/">
            Home
          </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/brand">
            Brands
          </nuxt-link>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style scoped>
</style>

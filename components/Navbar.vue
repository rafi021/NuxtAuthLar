<template>
<div>
  <b-navbar toggleable="lg" type="dark" variant="info">
  <b-navbar-brand to='/'>NavBar</b-navbar-brand>
      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-item-dropdown right>
          <!-- Using 'button-content' slot -->
          <template #button-content>
            <em>User</em>
          </template>
          <b-dropdown-item to="/dashboard">Dashboard</b-dropdown-item>
          <b-dropdown-item href="#" @click.prevent="logout()">Log Out</b-dropdown-item>
          <b-dropdown-item to="/login">login</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
  </b-navbar>
</div>
</template>

<script>
export default {
  methods: {
    logout () {
      console.log('logout!!!')
    }
  }
}
</script>

<style scoped>
</style>

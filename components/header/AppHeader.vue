<template>
  <b-navbar
    class="app-header"
    toggleable="lg"
    :type="$colorMode.value"
    :variant="$colorMode.value"
  >
    <b-navbar-brand to="/"> Find Mentor </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse" />

    <b-collapse id="nav-collapse" v-model="isCollapsed" is-nav>
      <b-navbar-nav>
        <app-register-button />
        <b-nav-item to="/guide/" active-class="active">
          How It Works?
        </b-nav-item>
        <b-nav-item exact active-class="active" to="/mentorships/">
          Active Mentorships
        </b-nav-item>
        <b-nav-item exact to="/mentees/" active-class="active">
          Mentees
        </b-nav-item>
        <b-nav-item exact to="/mentors/" active-class="active">
          Mentors
        </b-nav-item>
      </b-navbar-nav>
      <b-navbar-nav class="ml-auto" right>
        <app-search-input @searchTriggered="isCollapsed = false" />
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
  data() {
    return {
      isCollapsed: false,
    }
  },
}
</script>

<style scoped lang="scss">
.navbar-nav {
  align-items: center;
}
</style>

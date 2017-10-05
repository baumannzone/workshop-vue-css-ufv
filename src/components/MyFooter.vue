<template>
  <footer class="navbar fixed-bottom navbar-light bg-light">
    <div class="navbar text">
      <span class="badge badge-info">{{ active }} active users</span>
    </div>
  </footer>
</template>

<script>
  export default {
    name: 'my-footer',
    data() {
      return {
        active: 8,
      };
    },
  };
</script>

<style></style>

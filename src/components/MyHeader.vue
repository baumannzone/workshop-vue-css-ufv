<template>
  <header>
    <nav class="navbar navbar-expand-lg navbar-light bg-light fixed-top">
      <a href="#" class="navbar-brand"> {{ brand }}</a>
      <button type="button" data-toggle="collapse" data-target="#myNav" aria-controls="navbarSupportedContent"
              aria-expanded="false" aria-label="Toggle navigation" class="navbar-toggler">
          <span class="navbar-toggler-icon"></span>
      </button>
      <div id="myNav" class="collapse navbar-collapse justify-content-end">
        <div class="navbar-text">{{ user }}</div>
      </div>
    </nav>
  </header>

</template>

<script>
  export default {
    name: 'my-header',
    data() {
      return {
        brand: 'ACME Ltd.',
        user: 'Jorge Baumann',
      };
    },
  };
</script>

<style></style>

<template>
  <div class="col-sm-6 col-md-4 col-lg-3 d-flex mb-4">
    <div class="card">
      <div :style="{ backgroundImage: `url('${data.gifurl}')` }" class="card-body-img"></div>
      <div class="card-body">
        <p class="card-text">{{ data.title }}</p>
      </div>
      <div class="card-body d-flex justify-content-end align-items-end pt-0">
        <a :href="data.gifurl" class="btn btn-outline-primary btn-sm">Go</a>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'card',
    props: {
      data: Object,
    },
  };
</script>


<style>
  .card {
    width: 100%;
    transition: box-shadow 0.15s linear;
  }

  .card:hover {
    box-shadow: 0 0 6px 4px #dadada;
  }

  .card .card-body-img {
    min-height: 10rem;
    background-position: center;
    background-size: cover;
  }
</style>

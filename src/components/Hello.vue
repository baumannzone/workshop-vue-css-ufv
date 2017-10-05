<template>
  <div class="hello">
    <div class="row">
      <div class="col-md-12">
        <h1 class="mb-4">{{ msg }}</h1>
      </div>
    </div>
    <div class="row justify-content-start align-items-stretch">
      <card v-for="(card, index) in cards" :key="index" :data="card"></card>
    </div>
  </div>
</template>

<script>
  import axios from 'axios';
  import Card from './Card';

  export default {
    name: 'hello',
    components: {
      Card,
    },
    mounted() {
      axios.get( 'https://vue-workshop-ufv.firebaseio.com/data.json' )
        .then( ( response ) => {
          this.cards = response.data;
        } )
        .catch( ( e ) => {
          console.debug( e );
        } );
    },
    data() {
      return {
        msg: 'Nice pictures',
        cards: null,
      };
    },
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .hello {
    margin-top: 80px;
    margin-bottom: 80px;
  }
</style>

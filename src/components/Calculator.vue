<template>
  <div class="hello">
    <p>
    </p>
    
     <!-- <p># {{ count }}</p> -->
    <input v-model="input" placeholder="edit me">
    <button v-on:click.prevent="plus">+</button>
    <button v-on:click.prevent="minus">-</button>

    <p>= {{ calc }}</p>
  </div>
</template>

<script>
// user puts a input

export default {
  data: ()=> {
    return {
      steps: 0,
      input: null,
      calc: 0,
    }
  },
  methods: {
    plus () {
      this.steps++;
      this.calc = this.calc + parseInt(this.input)
    },
    minus () {
        this.steps++;
        this.calc = this.calc - parseInt(this.input)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

<template>
  <div class="container-fluid hello">
    <div class="row">
      <div class="col-12">
        <h1>{{ msg }}</h1>
        <p>
          <a href="https://cli.vuejs.org" target="_blank" rel="noopener"></a>.
        </p>
      </div>
    </div>
    <div class="row justify-content-center">
      <div class="col-12">
        <h1>Welcome to Slappy Slap</h1>
      </div>
    </div>
    <div class="row justify-content-center pt-5">
      <button type="button" class="btn btn-rounded btn-primary mx-1">
        Slap
      </button>
      <button type="button" class="btn btn-rounded btn-primary mx-1">
        Kick
      </button>
      <button type="button" class="btn btn-rounded btn-primary mx-1">
        Punch
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  methods: {},
};
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

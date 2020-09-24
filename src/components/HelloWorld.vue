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
    <div class="row">
      <div class="col-12">
        <h3>Health: {{ target.health }}</h3>
      </div>
    </div>
    <div class="row justify-content-center pt-5">
      <button
        type="button"
        class="btn btn-rounded btn-info mx-1"
        @click="attackTarget(attack.damage)"
        v-for="attack in attacks"
        :key="attack.name"
      >
        {{ attack.name }}
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
  data() {
    return {
      target: {
        health: 100,
      },
      attacks: [
        {
          name: "Slap",
          damage: "5",
        },
        {
          name: "Kick",
          damage: 10,
        },
        {
          name: "Punch",
          damage: 15,
        },
      ],
    };
  },
  methods: {
    attackTarget(damage) {
      this.target.health -= damage;
    },
  },
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

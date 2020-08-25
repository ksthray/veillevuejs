<template>
  <div class="container">
    <p>Salut {{user}}</p>
    <input type="text" v-model="user" />
    <br />
    <br />
    <div class="row">
      <div class="col-md-7">
        <h2>Liste des apprenants</h2>
        <ul v-for:="apprenant in apprenants">
          <li v-bind:for="apprenant">
            {{apprenant}}
            <button v-on:click="devfront(apprenant)" style="margin-left: 10px">frontend</button>
            <button v-on:click="devback(apprenant)" style="margin-left: 10px">backend</button>
          </li>
        </ul>
      </div>
      <div class="col-md-5">
        <h2>Section</h2>
        <div class="row">
          <div class="col-md-6">
            <h4 v-if="frontend.length > 0">Dev Frontend</h4>
            <div v-for:="item in frontend" style="color: orange;">
              <p v-bind:for="item">{{item}}</p>
              <br />
            </div>
            <strong v-if="frontend.length > 0">dans la kda il y a : {{frontend.length}} dev frontend</strong>
          </div>
          <div class="col-md-6">
            <h4 v-if="backend.length > 0">Dev Backend</h4>
            <div v-for:="item in backend" style="color: blue;">
              <p v-bind:for="item">{{item}}</p>
              <br />
            </div>
            <strong v-if="backend.length > 0">dans la kda il y a : {{backend.length}} dev backend</strong>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Section",
  data: () => ({
    user: "sarah lisangola",
    apprenants: [
      "claude",
      "sarah",
      "françois",
      "ben",
      "peniel",
      "osée",
      "murduch",
      "laurène",
      "gael",
      "stani",
      "joseph",
      "camille",
      "kalala",
      "manzako",
      "thesy",
      "semia",
      "russel",
      "dieu donnée",
      "axel",
    ],
    frontend: [],
    backend: [],
  }),
  mounted() {
    (function () {
      console.log("notre requete ajax");
    })();
  },
  methods: {
    devfront: function (apprenant) {
      this.frontend.push(apprenant);
    },
    devback: function (apprenant) {
      this.backend.push(apprenant);
    },
    getUrl: function () {
      console.log("notre requete ajax");
    },
  },
};
</script>

<style>
.row {
  border: 1px solid #ccc;
  padding: 10px;
}
</style>
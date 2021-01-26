<template>
  <div class="hello">
    <h1>Cordova {{ device.cordova }}</h1>
    <h2>{{ device.manufacturer }} {{ device.model }}</h2>
    <h2>{{ device.platform }} {{ device.version }}</h2>
    <h2>uuid: {{ device.uuid }}</h2>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      device: {}
    }
  },
  mounted() {
    document.addEventListener("deviceready", this.onDeviceReady);
  },
  beforeDestroy() {
    document.removeEventListener("deviceready", this.onDeviceReady);
  },
  methods: {
    onDeviceReady() {
      console.log(device);
      this.device = device
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

<template>
  <div class="hello">
    <div>{{count}}</div>
    <div @click="$store.commit('add')">add</div>
    <div @click="$store.commit('reduce')">reduce</div>
    <router-link to='/store'>to</router-link>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
    }
  },
  computed:{
    count(){
      return this.$store.state.count
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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

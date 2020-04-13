<template>
  <div class="hello">
    <div>{{count}}</div>
    <div @click="add(10)">add</div>
    <div @click="reduce">reduce</div>
  </div>
</template>

<script>
// import store from '@/store/index'
import { mapState, mapMutations, mapGetters, mapActions } from 'vuex'
export default {
  name: 'Store',
  data () {
    return {
    }
  },
  computed:{
      ...mapState(['count']),
      ...mapGetters(['count'])
  },
  methods:{
      ...mapMutations(['add','reduce']),
      ...mapActions(['addAction','reduceAction'])
  }
//   store
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

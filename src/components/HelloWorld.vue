<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h1>{{ name }}</h1>

    <p> 
    {{count}} 
    </p>
    <button @click="addCount">Add</button>
  </div>
</template>

<script>
import {mapState} from "vuex";
export default {
  name: 'HelloWorld',
  data(){
    return {
      name:"ahmed",
    };
  },
  props: {
    msg: String
  },
  computed: {
    ...mapState(["count"]),
  },
  methods:{
    addCount(){
      this.count ++
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
button {
  width: 50px;
  height: 50px;
  cursor: pointer;
}
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

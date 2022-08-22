<template>
  <div class="hello">
    <h1>Welcome {{firstname}} {{lastname}}</h1>
    <p>
      What is your name?
    </p>

    <p>First Name: <input type="text"   v-model="firstname" ></p>

    <p>Last Name: <input type="text"   v-model="lastname" ></p>

    <input type="radio" name="choice" v-model="dnd" value="1"> Dungeons
    <input type="radio" name="choice" v-model="dnd" value="2"> Dragons 
    <br>
    <img alt="Le Dungeon" src="../img/dungeon.png" v-if="dnd === '1'">
    <img alt="Dragon" src="../img/dragon.png" v-else-if="dnd === '2'">

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: function(){
    return {
      firstname: "", lastname: "", dnd: "" 
    }
  },
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

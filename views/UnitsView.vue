<template>
  <div>
    <h1>Units</h1>
    <table class="table">
      <thead>
        <tr>
          <th scope="col">Code</th>
          <th scope="col">Description</th>
          <th scope="col">CP</th>
          <th scope="col">Type</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(unit,index) in units" :key="index">
          <td>{{unit.code}}</td>
          <td>{{unit.desc}}</td>
          <td>{{unit.cp}}</td>
          <td>{{unit.type}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script> 
import Units from "../assets/units.json";        // your json file is under assets 
export default { 
  name: 'UnitS', 
  data: function(){ 
  return  {units:Units}  
 },
  mounted(){
    console.log(this.units)
  }
} 
</script> 
 
<!-- Add "scoped" attribute to limit CSS to this component only --> 
<style scoped> 
  
</style> 
<template>
  <div class="container">
    <div class="row">
        <p>
            <!-- Using textbox to get user input -->
            <b>
                <label for="status"> Status: <input type="text" name="status" id="status" v-model="strStatus"></label>
            </b>
            <!-- Using button to post status -->
            <button type="button" v-on:click="add(strStatus)">Post</button>
        </p>
    </div>

    <div class="row">
        <ul v-for="s in statPosts" :key="s">
            <li> 
                {{s}} <button type="button" v-on:click="remove(s)">Del</button>
            </li>
        </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TaskView',
  data:function(){ 
    return{ 
        statPosts:[], 
        strStatus:''
    } 
  },
  methods: { 
  add:function(status) { 
      //push status into statPosts array 
      this.statPosts.push(status);
  },
  remove:function(index){ 
      //delete status from statPost using index 
      var i = this.statPosts.indexOf(index);
      this.statPosts.splice(i, 1);
  }
}   
}

  
</script>
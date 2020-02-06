<template>
  <div class="container">
    <h1>Feed</h1>

    <collapse>
      <div style = "display: inline-block"> <img src="img/ryan.jpg" height="42" width="42"></div>
     <div style= "display: inline-block"> <collapse-item title="i wanna go skybording" name="1">
        <div  style = "display: inline-block">  m-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.</div>
      </collapse-item></div>
    </collapse>
    <h1>{{ msg }}</h1>
    <ul id="example-1">
      <ul id="v-for-object" class="demo">
        <div v-for="item in items" v-bind:key="item.id">
          {{item.name}}
          <br />
          {{item.Todo}}
          <br />
          <br />
        </div>
      </ul>
    </ul>
  </div>
</template>

<script>
import Collapse from './Collapse.vue'
import CollapseItem from './CollapseItem.vue'



export default {

  components: {
    Collapse,
    CollapseItem
  },

  name: "feed",
  props: {
    msg: String
  },
  data: function() {
    return {
      items: {
        user1: { name: "Jack", Todo: "Kill someone,Skydiving,Blabla " },
        user2: { name: "Tom", Todo: "Skydiving" },
        user3: { name: "Anna", Todo: "SnowBboarding" },
        user4: { name: "Mike", Todo: "blalba" },
        user5: { name: "Jack", Todo: "Kill someone,Skydiving,Blabla " },
        user6: { name: "Tom", Todo: "Skydiving" },
        user7: { name: "Anna", Todo: "SnowBboarding" },
        user8: { name: "Mike", Todo: "blalba" },
        user9: { name: "Jack", Todo: "Kill someone,Skydiving,Blabla " },
        user10: { name: "Tom", Todo: "Skydiving" },
        user11: { name: "Anna", Todo: "SnowBboarding" },
        user12: { name: "Mike", Todo: "blalba" }
      }
    };
  }
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

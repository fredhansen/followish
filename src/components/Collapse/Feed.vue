<template>
  <div class="hello">
    <h1>Feed</h1>
    <collapse>
      <collapse-item title="Default Collapsible Item 1" name="1">
        <div>11 pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.</div>
      </collapse-item>
      <collapse-item title="Default Collapsible Item 1" name="2">
        <div>Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.</div>
      </collapse-item>
      <collapse-item title="Default Collapsible Item 1" name="3">
        <div>Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.</div>
      </collapse-item>
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

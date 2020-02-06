<template>
  <div class="container">
    <div>
      <br />
      <fg-input placeholder="Search" v-model="inputVal"></fg-input>
    </div>
    <p>{{ inputVal }}</p>
    <div class="container button-container row justify-content-md-center">
      <n-button type="primary" class="btn btn-primary btn-round btn-sm">everything</n-button>
      <n-button type="info" class="btn btn-neutral btn-round btn-sm">winter sports</n-button>
      <n-button type="info" class="btn btn-neutral btn-round btn-sm">food</n-button>
      <n-button type="info" class="btn btn-neutral btn-round btn-sm">skydiving</n-button>
    </div>
    <div class="container text-center">
      <div class="row justify-content-md-center">
        <div class="col-md-12 col-lg-8">
          <h4 class="text-black bold">I've always wanted to...</h4>
        </div>
      </div>
    </div>

    <collapse>
      <collapse-item title="go snowboarding" name="1">
        <div>m-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.</div>
        <div class="button-container">
          <a href="#/profile" class="btn btn-primary btn-round btn-lg">view profile</a>
          <a href="#/profile" class="btn btn-primary btn-round btn-lg">message</a>
        </div>
      </collapse-item>
      <br />
      <div v-for="item in items" v-bind:key="item.title">
        <collapse-item v-bind:title="item.title">
          <div>{{item.content}}</div>

          <div class="button-container">
            <a href="#/profile" class="btn btn-primary btn-round btn-lg">view profile</a>
            <a href="#/profile" class="btn btn-primary btn-round btn-lg">message</a>
          </div>
        </collapse-item>
        <br />
      </div>
    </collapse>

    <div class="section">
      <div class="container text-center">
        <div class="row justify-content-md-center">
          <div class="col-md-12 col-lg-8">
            <h2 class="title">No more adventures here...</h2>
            <h5 class="description">Maybe add some new ones?</h5>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Collapse from "./Collapse.vue";
import CollapseItem from "./CollapseItem.vue";
import FgInput from "../Inputs/formGroupInput";
import Button from "../Button";

export default {
  components: {
    Collapse,
    CollapseItem,
    FgInput,
    Button
  },

  name: "feed",
  props: {
    msg: String
  },
  data: function() {
    return {
      inputVal: "",

      items: {
        user1: {
          name: "Jack",
          title: "ride a bull",
          content: "aa"
        },
        user2: { name: "Tom", title: "go skydiving", content: "aa" },
        user3: { name: "Anna", title: "try Georgian food", content: "aa" }
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

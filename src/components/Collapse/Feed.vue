<template>
  <div class="container">
    <div>
      <br />
      <fg-input placeholder="Search" v-model="inputVal"></fg-input>
    </div>
    <p>{{ inputVal }}</p>
   
    <div class="container text-center">
      <div class="row justify-content-md-center">
        <div class="col-md-12 col-lg-8">
          <h4 class="text-black bold">I've always wanted to...</h4>
        </div>
      </div>
    </div>

    <tabs type="primary">
      <tab-pane label=" sports">
        <collapse>
          <div v-for="item in items" v-bind:key="item.title">
            <collapse-item class="container" v-bind:title="item.title" v-bind:name="item.name">
              <div>{{item.content}}</div>

              <div class="button-container">
                <a href="#/profile" class="btn btn-primary btn-round btn-lg">view profile</a>
                <a href="#/profile" class="btn btn-primary btn-round btn-lg">message</a>
              </div>
            </collapse-item>
            <br />
          </div>
        </collapse>
      </tab-pane>

      <tab-pane label="Skydiving">
        <collapse>
          <div v-for="item in items2" v-bind:key="item.title">
            <collapse-item class="container" v-bind:title="item.title" v-bind:name="item.name">
              <div>{{item.content}}</div>

              <div class="button-container">
                <a href="#/profile" class="btn btn-primary btn-round btn-lg">view profile</a>
                <a href="#/profile" class="btn btn-primary btn-round btn-lg">message</a>
              </div>
            </collapse-item>
            <br />
          </div>
        </collapse>
      </tab-pane>

      <tab-pane label="Food">
        <collapse>
          <div v-for="item in items3" v-bind:key="item.title">
            <collapse-item class="container" v-bind:title="item.title" v-bind:name="item.name">
              <div>{{item.content}}</div>

              <div class="button-container">
                <a href="#/profile" class="btn btn-primary btn-round btn-lg">view profile</a>
                <a href="#/profile" class="btn btn-primary btn-round btn-lg">message</a>
              </div>
            </collapse-item>
            <br />
          </div>
        </collapse>
      </tab-pane>
    </tabs>

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
import {Tabs, TabPane} from '@/components';

export default {
  components: {
    Collapse,
    CollapseItem,
    FgInput,
    Button,
    Tabs,
    TabPane
  },

  name: "feed",
  props: {
    msg: String
  },
  data: function() {
    return {
      inputVal: "",

      items: {
        user0: {
          name: "Ryan Scheinder",
          title: "go snowboarding",
          content:
            "I want to try out snowboarding before I'm 30. None of my friends are open to learning and I don't really want to get an instructor."
        },
        user1: {
          name: "Jack Daniel",
          title: "ride a bull",
          content: "aa"
        },
        user2: { name: "Tom Brady", title: "go skydiving", content: "aa" },
        user3: {
          name: "Tasneem Haque",
          title: "try Georgian food",
          content: "aa"
        },
        user4: {
          name: "Marina Sarapuu",
          title: "try Georgian food",
          content: "aa"
        },
        user5: {
          name: "Samuel Sanchez",
          title: "try Georgian food",
          content: "aa"
        },
        user6: {
          name: "Pavel Valge",
          title: "try Georgian food",
          content: "aa"
        }
      },
      items2: {
        user0: {
          name: "Karim Scheinder",
          title: "ride a bull",
          content:
            "I want to try out snowboarding before I'm 30. None of my friends are open to learning and I don't really want to get an instructor."
        },
        user1: {
          name: "Anna Danni",
          title: "ride a bull",
          content: "aa"
        },
        user2: { name: "Tom Brady", title: "go skydiving", content: "aa" },
        user3: {
          name: "Tasneem Haque",
          title: "try Georgian food",
          content: "aa"
        },
        user4: {
          name: "Marina Sarapuu",
          title: "try Georgian food",
          content: "aa"
        },
        user5: {
          name: "Samuel Sanchez",
          title: "try Georgian food",
          content: "aa"
        },
        user6: {
          name: "Pavel Valge",
          title: "try Georgian food",
          content: "aa"
        }
      },
      items3: {
        user0: {
          name: "Mark Rhian",
          title: "try Mexican food",
          content:
            "I want to try out snowboarding before I'm 30. None of my friends are open to learning and I don't really want to get an instructor."
        },
        user1: {
          name: "Jack Daniel",
          title: "ride a bull",
          content: "aa"
        },
        user2: { name: "Tom Brady", title: "go skydiving", content: "aa" },
        user3: {
          name: "Tasneem Haque",
          title: "try Georgian food",
          content: "aa"
        },
        user4: {
          name: "Marina Sarapuu",
          title: "try Georgian food",
          content: "aa"
        },
        user5: {
          name: "Samuel Sanchez",
          title: "try Georgian food",
          content: "aa"
        },
        user6: {
          name: "Pavel Valge",
          title: "try Georgian food",
          content: "aa"
        }
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

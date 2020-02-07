<template>
  <div class="btn btn-round btn-info btn-lg">
    <div role="tab" id="headingOne">
      <a
        data-toggle="collapse"
        data-parent="#accordion"
        :href="`#${itemId}`"
        @click.prevent="activate"
        :aria-expanded="active"
        :aria-controls="`content-${itemId}`"
      >
        <div align="left">
          <div name="image">
            <img class="rounded-circle img-padding" src="img/ryan.jpg" height="70" width="70" align="left" />
          </div>

          <div >
            <ul>
              <div name="name" class="text-black bold">{{ name }}</div>
              <div name="title" class="text-black bold large">
                {{ title }}
                <i v-if="!noIcon" class="now-ui-icons arrows-1_minimal-down"></i>
              </div>
              <div name="icon"></div>
            </ul>
          </div>
        </div>
      </a>
    </div>
    <collapse-transition :duration="animationDuration">
      <div
        v-show="active"
        :id="`content-${itemId}`"
        role="tabpanel"
        :aria-labelledby="title"
        class="collapsed"
      >
        <div class="card-body text-black">
          <slot></slot>
        </div>
      </div>
    </collapse-transition>
  </div>
</template>
<script>
import { CollapseTransition } from "vue2-transitions";

export default {
  name: "collapse-item",
  components: {
    CollapseTransition
  },
  props: {
    title: {
      type: String,
      default: ""
    },
    name: {
      type: String,
      default: ""
    },
    id: String,
    noIcon: Boolean
  },
  inject: {
    animationDuration: {
      default: 250
    },
    multipleActive: {
      default: false
    },

    deactivateAll: {
      default: () => {}
    }
  },
  computed: {
    itemId() {
      return this.id || this.title;
    }
  },
  data() {
    return {
      active: false
    };
  },
  methods: {
    activate() {
      if (!this.multipleActive) {
        this.deactivateAll();
      }
      this.active = !this.active;
    }
  },
  mounted() {
    this.addItem(this);
  },
  destroyed() {
    if (this.$el && this.$el.parentNode) {
      this.$el.parentNode.removeChild(this.$el);
    }
    this.removeItem(this);
  }
};
</script>
<style></style>

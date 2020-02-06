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
        <slot name="image">
          <div>
            <img class="rounded-circle" src="img/ryan.jpg" height="42" width="42" />
          </div>
        </slot>
        <span name="title" class="text-black title h4">{{ title }}</span>
        <slot name="icon">
          <i v-if="!noIcon" class="now-ui-icons arrows-1_minimal-down"></i>
        </slot>
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

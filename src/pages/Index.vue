<template>
  <div>
    <div class="page-header clear-filter" filter-color="wish-orange">
      <parallax class="page-header-image" style="background-image:url('img/header.jpg')"></parallax>
      <div class="container">
        <div class="content-center brand">
          <img class="n-logo" src="img/now-logo.png" alt />
          <h1 class="h1"></h1>
          <h3>followish;</h3>
          <div class="button-container">
            <a href="#/login" class="btn btn-danger btn-round btn-lg">Get started</a>
            <br />
            <a v-on:click="scrollToFeed" class="now-ui-icons arrows-1_minimal-down"></a>
          </div>
        </div>
      </div>
    </div>
    <div class="main"></div>

    <feed id="feed"></feed>
    <!-- 
<feed></feed>
    <basic-elements></basic-elements>
    <navigation></navigation>
    <tabs-section></tabs-section>
    <progress-pagination></progress-pagination>
    <notifications></notifications>
    <typography></typography>
    <javascript-components></javascript-components>
    <carousel-section></carousel-section>
    <nucleo-icons-section></nucleo-icons-section>

    -->

    <!-- 
    <signup-form></signup-form>
    <examples-section></examples-section>
    <download-section></download-section>
    -->
  </div>
</template>
<script>
import { Parallax } from "@/components";
import BasicElements from "./components/BasicElementsSection";
import Feed from "../components/Collapse/Feed";
import Navigation from "./components/Navigation";
import TabsSection from "./components/Tabs";
import ProgressPagination from "./components/ProgressPagination";
import Notifications from "./components/Notifications";
import Typography from "./components/Typography";
import JavascriptComponents from "./components/JavascriptComponents";
import CarouselSection from "./components/CarouselSection";
import NucleoIconsSection from "./components/NucleoIconsSection";
import SignupForm from "./components/SignupForm";
import ExamplesSection from "./components/ExamplesSection";
import DownloadSection from "./components/DownloadSection";
import Button from "../components/Button";

export default {
  name: "index",
  bodyClass: "index-page",
  components: {
    [Button.name]: Button,
    Feed,
    Parallax,
    BasicElements,
    Navigation,
    TabsSection,
    ProgressPagination,
    Notifications,
    Typography,
    JavascriptComponents,
    CarouselSection,
    NucleoIconsSection,
    SignupForm,
    ExamplesSection,
    DownloadSection
  },
  methods: {
    scrollToFeed() {
      var container = this.$el.querySelector("#feed");
      container.scrollTop = container.scrollHeight;
      console.log("aaaa");
    }
  }
};
</script>
<style></style>

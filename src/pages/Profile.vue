<template>
  <div>
    <div class="page-header clear-filter" filter-color="wish-orange">
      <parallax class="page-header-image" style="background-image:url('img/bg5.jpg')"></parallax>
      <div class="container">
        <div class="photo-container">
          <img src="img/ryan.jpg" alt />
        </div>
        <h3 class="title">Ryan Scheinder</h3>
        <p class="category">Photographer</p>
        <p class="category">Tartu</p>
        <div class="content">
          <div class="social-description">
            <h2>6</h2>
            <p>Wishes</p>
          </div>
          <div class="social-description">
            <h2>48</h2>
            <p>Mutual friends</p>
          </div>
        </div>
      </div>
    </div>
    <div class="section">
      <div class="container">
        <div class="button-container">
          <a href="#button" class="btn btn-primary btn-round btn-lg">Chat</a>
          <a
            href="#button"
            class="btn btn-default btn-round btn-lg btn-icon"
            rel="tooltip"
            title="Facebook"
          >
            <i class="fab fa-facebook"></i>
          </a>
        </div>
        <div class="row">
          <div class="col-md-6 ml-auto mr-auto">
            <h3 class="title">I've always wanted to...</h3>
            <h5 class="description">List the things you want to do with someone</h5>

            <collapse>
              <collapse-item title="learn snowboarding" name="1">
                <div>I want to try out snowboarding before I'm 30. None of my friends are open to learning and I don't really want to get an instructor.</div>
              </collapse-item>
            </collapse>
          </div>
        </div>

        <div class="row">
          <div class="col-md-6 ml-auto mr-auto">
            <h4 class="title text-center">Wishes that have come true</h4>
            <h5 class="description">Post pictures of the things you have already done</h5>
          </div>
          <tabs
            pills
            class="nav-align-center"
            tab-content-classes="gallery"
            tab-nav-classes="nav-pills-just-icons"
            type="primary"
          >
            <tab-pane title="Profile">
              <i slot="label" class="now-ui-icons design_image"></i>

              <div class="col-md-10 ml-auto mr-auto">
                <div class="row collections">
                  <div class="col-md-6">
                    <img src="img/bg6.jpg" class="img-raised" />
                    <img src="img/bg11.jpg" alt class="img-raised" />
                  </div>
                  <div class="col-md-6">
                    <img src="img/bg7.jpg" alt class="img-raised" />
                    <img src="img/bg8.jpg" alt class="img-raised" />
                  </div>
                </div>
              </div>
            </tab-pane>

            <tab-pane title="Home">
              <i slot="label" class="now-ui-icons location_world"></i>

              <div class="col-md-10 ml-auto mr-auto">
                <div class="row collections">
                  <div class="col-md-6">
                    <img src="img/bg1.jpg" alt class="img-raised" />
                    <img src="img/bg3.jpg" alt class="img-raised" />
                  </div>
                  <div class="col-md-6">
                    <img src="img/bg8.jpg" alt class="img-raised" />
                    <img src="img/bg7.jpg" alt class="img-raised" />
                  </div>
                </div>
              </div>
            </tab-pane>

            <tab-pane title="Messages">
              <i slot="label" class="now-ui-icons sport_user-run"></i>

              <div class="col-md-10 ml-auto mr-auto">
                <div class="row collections">
                  <div class="col-md-6">
                    <img src="img/bg3.jpg" alt class="img-raised" />
                    <img src="img/bg8.jpg" alt class="img-raised" />
                  </div>
                  <div class="col-md-6">
                    <img src="img/bg7.jpg" alt class="img-raised" />
                    <img src="img/bg6.jpg" class="img-raised" />
                  </div>
                </div>
              </div>
            </tab-pane>
          </tabs>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { Tabs, TabPane } from "@/components";
import Collapse from "../components/Collapse/Collapse";
import CollapseItem from "../components/Collapse/CollapseItem";

export default {
  name: "profile",
  bodyClass: "profile-page",
  components: {
    Tabs,
    TabPane,
    Collapse,
    CollapseItem
  }
};
</script>
<style></style>

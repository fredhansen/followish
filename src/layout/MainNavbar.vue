<template>
  <navbar
    position="fixed"
    type="white"
    :transparent="transparent"
    :color-on-scroll="colorOnScroll"
    menu-classes="ml-auto"
  >
    <template slot-scope="{ }"> <!-- toggle, isToggled -->
      <router-link class="navbar-brand" to="/">
        Adventures
      </router-link>
      <el-popover
        ref="popover1"
        popper-class="popover"
        placement="bottom"
        width="200"
        trigger="hover"
      >
        <div class="popover-body">
        </div>
      </el-popover>
    </template>
    <template slot="navbar-menu">
      <li class="nav-item">
        <nav-link class="nav-link" to="/profile">
          <i class="now-ui-icons users_single-02"></i> Profile
        </nav-link>
      </li>
      <li class="nav-item">
        <nav-link class="nav-link" to="/">
          <i class="now-ui-icons education_paper"></i> Potential adventures
        </nav-link>
      </li>
      
    </template>
  </navbar>
</template>

<script>
import { DropDown, NavbarToggleButton, Navbar, NavLink } from '@/components';
import { Popover } from 'element-ui';
export default {
  name: 'main-navbar',
  props: {
    transparent: Boolean,
    colorOnScroll: Number
  },
  components: {
    DropDown,
    Navbar,
    NavbarToggleButton,
    NavLink,
    [Popover.name]: Popover
  }
};
</script>

<style scoped></style>

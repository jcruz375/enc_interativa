<template>
  <aside v-if="isDrawerOpen" class="drawer">
    <ul>
      <li @click="toggleDrawer()">
        <a  href="#">HOME</a>
      </li>
      <li @click="toggleDrawer()">
        <a href="#">COMO PARTICIPAR</a>
      </li>
      <li @click="toggleDrawer()">
        <a href="#">PRÊMIOS</a>
      </li>
      <li @click="toggleDrawer()">
        <a href="#">PRODUTOS PARTICIPANTES</a>
      </li>
      <li @click="toggleDrawer()">
        <a href="#">RECEITAS</a>
      </li>
      <li @click="toggleDrawer()">
        <a href="#">PÍLULAS NBA</a>
      </li>
      <li @click="toggleDrawer()">
        <a href="#">GANHADORES</a>
      </li>
      <li>
        <ProfileDropdown />
      </li>
    </ul>
  </aside>
</template>

<script>
import ProfileDropdown from './profile_dropdown.vue';

export default {
  components: {
    ProfileDropdown
  },  
  props: {
    isDrawerOpen: Boolean,
    handleToggleDrawerOpen: Function,
  },
  methods: {
    toggleDrawer() {
      this.handleToggleDrawerOpen(!this.isDrawerOpen);
    }
  }
};
</script>

<style lang="scss" scoped>
.drawer {
  position: fixed;
  top: 0;
  left: 0;
  width: 250px;
  height: 100%;
  background-color: #074a75;
  padding: 32px;
  box-shadow: 2px 0 5px rgba(0, 0, 0, 0.2);
  z-index: 10;

  ul {
    list-style-type: none;
    text-align: left;
    display: flex;
    flex-direction: column;
    gap: 20px;

    li {
      a {
        color: #FFFFFF;
        text-decoration: none;
        font-family: Brandon;
      }
    }
  }
}
</style>
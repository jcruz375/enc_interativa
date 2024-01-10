<template>
  <header>
    <ul class="desktop-links">
      <li>
        <a href="#">HOME</a>
      </li>
      <li>
        <a href="#">COMO PARTICIPAR</a>
      </li>
      <li>
        <a href="#">PRÊMIOS</a>
      </li>
      <li>
        <a href="#">PRODUTOS PARTICIPANTES</a>
      </li>
      <li>
        <a href="#">RECEITAS</a>
      </li>
      <li>
        <a href="#">PÍLULAS NBA</a>
      </li>
      <li>
        <a href="#">GANHADORES</a>
      </li>
      <li>
        <ProfileDropdown />
      </li>
    </ul>
    <button @click="handleToggleDrawerOpen(!isDrawerOpen)">
      <img src="../assets/icons/menu-mobile.png" alt="icone menu hambúrguer">
    </button>
    <DrawerComponent :isDrawerOpen="isDrawerOpen" :handleToggleDrawerOpen="handleToggleDrawerOpen"/>
  </header>
</template>

<script>
import ProfileDropdown from './profile_dropdown.vue'
import DrawerComponent from './drawer_component.vue';

import { ref } from 'vue';

export default {
  components: {
    ProfileDropdown,
    DrawerComponent
  },
  setup() {
    const isDrawerOpen = ref(false);

    function handleToggleDrawerOpen(drawerVisibility) {
      isDrawerOpen.value = drawerVisibility
      console.log(isDrawerOpen.value);
    }

    return {
      isDrawerOpen,
      handleToggleDrawerOpen,
    }
  }
}
</script>

<style lang="scss">
  header {
    width: 100%;
    height: 56px;
    background-color: #facc1f;

    button {
      display: none;
    }
    
    .desktop-links {
      width: inherit;
      height: inherit;
      
      display: flex;
      justify-content: center;
      
      list-style-type: none;
      li {

        height: 100%;
        max-width: 180px;
        padding: 0 16px;
        display: flex;
        align-items: center;
        box-sizing: border-box;
        font-size: 20px;
        line-height: 20px;
        
        transition: 0.3s;
        &:hover {
          background-color: #074a75;
          a {
            color: #facc1f;
          }
          .menu-title {
            color: #facc1f;
          }
          .arrow-icon {
            border-color: #facc1f;
          }
        }
        
        a {
          color: #074a75;
          font-size: 20px;
          text-decoration: none;
        }
      }
    }
  }

  @media (max-width: 768px) {
    header {
      display: flex;
      justify-content: flex-start;
      padding: 0 24px;
      .desktop-links {
        display: none;
      }
      button {
        display: block;
        background: transparent;
        border: none;
      }
    }
  }
</style>
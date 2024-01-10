<template>
  <div class="menu-container">
    <div class="menu-title" @click="toggleMenu">
      <span>Olá, {{ username }}</span>
      <i :class="['arrow-icon', { 'arrow-up': isMenuOpen }]"></i>
    </div>
    <ul v-if="isMenuOpen" class="menu-options">
      <li><a href="#">Opção 1</a></li>
      <li><a href="#">Opção 2</a></li>
      <li><a href="#">Opção 3</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
      username: 'Ana',
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
  },
};
</script>

<style lang="scss">
.menu-container {
  position: relative;
}

.menu-title {
  cursor: pointer;
  display: flex;
  align-items: center;

  font-size: 20px;
  font-family: Brandon;
  color: #074a75;

  // transition: 0.2s;
  // &:hover {
  //   color: #facc1f;
  // }
}

.arrow-icon {
  margin-left: 5px;
  border: solid black;
  border-width: 0 2px 2px 0;
  display: inline-block;
  padding: 3px;
  transition: transform 0.3s;
  border-color: #074a75;
  transform: rotate(46deg);
}

.arrow-up {
  transform: rotate(-135deg);
}

.menu-options {
  list-style-type: none;
  padding: 0;
  margin: 0;
  border: 1px solid #ccc;
  border-radius: 4px;
  position: absolute;
  top: 100%;
  left: 0;
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  display: none;
}

.menu-options li {
  padding: 8px;
}

.menu-options a {
  text-decoration: none;
  color: #333;
}
</style>

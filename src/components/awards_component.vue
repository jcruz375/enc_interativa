<template>
  <BlueContainer class="awards-section">
    <h3>compre, junte e troque</h3>
    <div class="selector-container">
      <ul>
        <li :class="{ selected: isSelected('plates')}" @click="setSelectedCategory('plates')">pratos</li>
        <li :class="{ selected: isSelected('bowls')}" @click="setSelectedCategory('bowls')">bowls</li>
        <li :class="{ selected: isSelected('board')}" @click="setSelectedCategory('board')">tábua</li>
      </ul>
    </div>
    <div class="galery-container">
      <img
        :class="{ selected: isSelected('plates')}"
        src="../assets/awards/galeria-pratos.png"
        alt="imagem dos pratos da campanha"
      >
      <img
        :class="{ selected: isSelected('bowls')}"
        src="../assets/awards/galeria-bowls.png"
        alt="imagem dos bowls da campanha"
      >
      <img
        :class="{ selected: isSelected('board')}"
        src="../assets/awards/galeria-tabua.png"
        alt="imagem da tábua da campanha"
      >
    </div>
  </BlueContainer>
</template>

<script>
import { ref } from 'vue'
import BlueContainer from "./blue_container.vue";
export default {
  components: {
    BlueContainer,
  },
  setup() {
    const selectedCategory = ref('plates');

    function setSelectedCategory(category) {
      selectedCategory.value = category;
      console.log(category);
    }

    const isSelected = (category) => {
      if (selectedCategory.value == category) {
        return true;
      }
      return false;
    }

    return {
      setSelectedCategory,
      isSelected
    }
  }
};
</script>

<style lang="scss" scoped>
.awards-section {
  h3 {
    font-size: var(--title-regular);
    color: #facc1f;
    font-family: Brandon;
    margin-bottom: 24px;
    text-transform: uppercase;
  }

  .selector-container {
    display: flex;
    justify-content: center;
    ul {
      display: flex;
      align-items: center;
      gap: 32px;
      padding: 4px;
      background-color: #074a75;
      list-style: none;
      font-size: 16px;
      border-radius: 32px;
      text-transform: uppercase;
      font-family: Brandon;
      color: #fff;
      cursor: pointer;
      margin-bottom: 24px;

      .selected {
        background-color: #facc1f;
        color: #074a75;
      }

      li {
        border-radius: 16px;
        padding: 4px 24px;
      }
    }
  }

  .galery-container {
    display: flex;
    justify-content: center;

    img {
      display: none;

      &.selected {
        display: block;
      }
    }
  }
}
</style>
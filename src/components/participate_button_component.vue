<template>
  <button>participe</button>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
button {
  color: #074a75;
  background-color: #facc1f;
  font-family: Brandon;
  font-size: var(--title-large);
  text-transform: uppercase;
  padding: 16px 40px;
  border-radius: 60px;
  border: none;
  box-shadow: 4px 4px 8px rgba(0, 0, 0, 0.6);
  cursor: pointer;
}

@media(max-width: 767px) {
  button {
    font-size: var(--text-regular);
  }
}
</style>
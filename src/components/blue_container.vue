<template>
  <section class="blue-container">
    <div class="intern-container">
      <slot></slot>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" >
.blue-container {
  background-color: #122641;
  border-radius: 40px;
  // position: relative;
  // bottom: 32px;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 24px;

  .intern-container {
    width: 100%;
    min-height: 100%;
    background-color: #122641;
    border: 4px solid #074a75;
    border-radius: 36px;
    padding: 36px 16px;
  }
}
</style>
<template>
  <section class="footer-section">
    <div class="bow-container">
      <hr />
      <img src="../assets/footer/laco.png" alt="laço" />
      <hr />
    </div>
    <article>
      <h2>Dúvidas</h2>
      <h2>Regulamento</h2>
    </article>
    <article>
      <img src="../assets/footer/redes-twitter.png" alt="link para twitter">
      <img src="../assets/footer/redes-instagram.png" alt="link para instagram">
      <img src="../assets/footer/redes-facebook.png" alt="link para facebook">
      <img src="../assets/footer/redes-yt.png" alt="link para you tube">
    </article>
    <article>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nulla recusandae architecto quae, quas, exercitationem ab adipisci vel alias vero sunt repellendus. Sequi, quas molestiae est nostrum nobis ratione animi enim!
    </article>
    <article>
      <img src="../assets/footer/unilever.png" alt="logo unilever">
    </article>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.footer-section {
  padding: 0 32px;
  display: flex;
  flex-direction: column;
  align-items: center;
  .bow-container {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;

    hr {
      width: 50%;
    }
  }

  article {
    display: flex;
    justify-content: center;
    gap: 64px;
    padding: 24px;
    font-family: Brandon;
    color: #FFFFFF;

    h2 {
      font-size: 20px;
      cursor: pointer;
    }

    p {
      font-size: var(--text-large);
    }
    &:last-child {
      padding-top: 0;
    }
  }
}
</style>
<template>
  <div id="app">
    <HeaderComponent />
    <section class="home-section">
      <article>
        <img
          src="./assets/home/logo-promo.png"
          alt="logo da promoção hellmann's"
        />
      </article>
      <article>
        <div class="unilever-logo">
          <img src="./assets/home/logo-unilever.png" alt="logo unilever" />
        </div>
        <PaticipateButton />
        <div class="produtos">
          <img
            src="./assets/home/produtos-home.png"
            alt="Produtos da promoção"
          />
        </div>
      </article>
    </section>
    <BlueContainer class="awards-example-section">
      <img
        src="./assets/awards/premios.png"
        alt="logo da promoção hellmann's"
      />
    </BlueContainer>
    <section class="how-to-participate">
      <h3>como participar</h3>
      <div class="steps">
        <img
          src="./assets/participate/passo-1.png"
          alt="1 - Cadastre-se aqui no site"
        />
        <img
          src="./assets/participate/passo-2.png"
          alt="2 - Acerte a bola no jogo para ganhar o NBA league pass - enquanto durarem os estoques"
        />
        <img
          src="./assets/participate/passo-3.png"
          alt="3 - Faça upload de sua nota fiscal"
        />
        <img
          src="./assets/participate/passo-4.png"
          alt="1 - Junte sextas e troque por premios"
        />
      </div>
      <div class="extras">
        <img
          src="./assets/participate/extra-1.png"
          alt="qualquer squeeze Helmann's - 1 cesta"
        />
        <img
          src="./assets/participate/extra-2.png"
          alt="squeeze suprema - 3 cestas"
        />
        <img
          src="./assets/participate/extra-3.png"
          alt="um ou mais Ruffles sabor cheeseburguer ou hot dog - no mesmo cupom fiscal que um squeeze Helmann's - 2 cestas extras"
        />
        <img
          src="./assets/participate/extra-4.png"
          alt="comprando na hamburgueria Helmann's - 1 cesta SP capital - Botão compre aqui"
        />
      </div>
      <PaticipateButton />
    </section>
    <AwardsComponent />
    <section class="movie-section">
      <span>
        dos dribles e enterradas memoráveis ao zerar do cronômetro,
        <br />
        <strong>
          cada hora h da nba fica ainda mais saborosa com hellman's</strong
        >
      </span>
      <h3>assista ao filme abaixo:</h3>
      <iframe
        class="video-player"
        src="https://www.youtube.com/embed/KAIR1_wOJvg?si=YgG-Y8LUOX-DKOMD"
        title="video promocional"
        frameborder="none"
      ></iframe>
    </section>
    <BlueContainer class="products-section">
      <h2>produtos participantes</h2>
      <h3>todos os squeezes da linha Helmann's</h3>
      <img src="./assets/home/produtos-home.png" alt="Produtos da promoção" />
    </BlueContainer>
    <section class="buy-now">
      <h2>compre agora e participe</h2>
      <div class="stores-container">
        <article>
          <img src="./assets/buy-now/pda.png" alt="Logo grupo pão de Açúcar" />
          <button class="store-button">GPA</button>
        </article>
        <article>
          <img
            src="./assets/buy-now/carrefour.png"
            alt="Logo grupo pão de Açúcar"
          />
          <button class="store-button">carrefour</button>
        </article>
      </div>
    </section>
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from "./components/header_component.vue";
import BlueContainer from "./components/blue_container.vue";
import AwardsComponent from "./components/awards_component.vue";
import PaticipateButton from "./components/participate_button_component.vue";
import FooterComponent from './components/footer_component.vue';

export default {
  name: "App",
  components: {
    HeaderComponent,
    BlueContainer,
    AwardsComponent,
    PaticipateButton,
    FooterComponent,
  },
};
</script>

<style lang="scss">
html,
body,
ul {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font-family: Brandon;
}

@font-face {
  font-family: "Latino";
  src: url("~@/assets/fonts/Latinotype - TrendSansFive.otf");
}

@font-face {
  font-family: "Brandon";
  src: url("~@/assets/fonts/Brandon Grotesque Black.otf");
}

:root {
  --text-large: 16px;
  --text-regular: 12px;
  --title-large: 44px;
  --title-regular: 36px;
}

#app {
  width: 100vw;
  max-width: 100%;
  min-height: 100vh;
  text-align: center;
  background-color: #074a75;
  box-sizing: border-box;
  overflow: hidden;
}

.home-section {
  background-image: url("./assets/bg-azul.jpg");
  max-height: 100vh;
  padding: 24px 0 0 0;

  display: flex;

  article {
    &:first-child {
      position: relative;
      left: 60px;
    }
    &:last-child {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
      position: relative;
      right: 60px;

      .unilever-logo {
        width: 75%;
        display: flex;
        justify-content: flex-end;
      }
      .produtos {
        // width: 58%;
        display: flex;
        justify-content: flex-end;
      }
    }
  }
}

.awards-example-section {
  position: relative;
  bottom: 32px;
}

.how-to-participate {
  padding: 32px 0;
  h3 {
    color: #ffffff;
    font-size: var(--title-regular);
    font-family: Latino;
    text-decoration: underline;
    text-underline-offset: 8px;
    padding: 4px;
    text-transform: uppercase;
  }

  .steps {
    margin: 32px 88px;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
  }

  .extras {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-evenly;
    margin: 0 128px;

    img {
      &:last-child {
        cursor: pointer;
      }
    }
  }
}

.movie-section {
  padding: 32px 0;
  span {
    font-size: var(--title-regular);
    font-family: Brandon;
    color: #ffffff;
    text-transform: uppercase;
    font-weight: 400;

    strong {
      font-weight: bold;
    }
  }

  h3 {
    font-size: var(--title-large);
    font-family: Brandon;
    color: #ffffff;
    text-transform: uppercase;
    margin-bottom: 24px;
  }
  .video-player {
    width: 70%;
    height: 490px;
  }
}

.products-section {
  position: relative;
  z-index: 1;

  h2 {
    font-family: Latino;
    font-size: var(--title-regular);
    color: #ffffff;
    text-decoration: underline;
    text-underline-offset: 8px;
    text-transform: uppercase;
    margin-bottom: 16px;
  }
  h3 {
    font-family: Brandon;
    font-size: var(--title-regular);
    color: #ffffff;
    text-transform: uppercase;
  }

  img {
    position: relative;
    top: 70px;
  }
}

.buy-now {
  padding-bottom: 64px;
  position: relative;
  background-image: url("./assets/bg-azul.jpg");
  bottom: 64px;
  z-index: 0;

  h2 {
    font-family: Latino;
    font-size: var(--title-regular);
    color: #ffffff;
    text-decoration: underline;
    text-underline-offset: 8px;
    text-transform: uppercase;
    margin-bottom: 16px;
    padding: 48px;
  }

  .stores-container {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 64px;

    button {
      width: 160px;
      padding: 16px;
      border-radius: 60px;
      margin-top: 24px;
      color: #074a75;
      background-color: #facc1f;
      font-family: Brandon;
      font-size: var(--text-large);
      cursor: pointer;
      border: none;
      box-shadow: 4px 4px 8px rgba(0, 0, 0, 0.6);
      text-transform: uppercase;
    }
    article {
      display: flex;
      justify-content: center;
      flex-direction: column;
      align-items: center;
    }
  }
}
</style>

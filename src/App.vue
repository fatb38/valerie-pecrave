<script setup lang="ts">
import FacebookIcon from '~icons/mdi/facebook'
</script>

<template>
  <header>
    <h2 id="title" class="secondary-color">Valérie Pecrave</h2>
    <img class="logo" src="/logo-valoche.jpg" alt="logo" width="90">
  </header>
  <main>
    <h2>Directrice de campagne officielle du groupe Eight Sins</h2>
    <h2 class="primary-color">En appel à votre générosité</h2>

    <a href="#">
      <button class="button" role="button">FAIRE UN DON</button>
    </a>
    <div class="speech-container">
      <div>
        <img id="main-photo" src="/valoche.jpg" alt="Valerie Pecrave" width="300">
      </div>
      <div class="speech">
        <p class="bold">Le groupe Eight Sins a besoin de vous aujourd'hui pour boucler le budget de financement de son
          nouvel album.</p>
        <p class="bold">Valoche et toute son équipe de campagne font appel à vous, cher public, pour aider le groupe à
          apporter une nouvelle fraicheur <span class="primary-color">Thrash Metal</span> dans cette scène tant malmenée
          depuis la Covid Party
          2020-2021.</p>
        <p class="bold">Pour que la France retrouve sa grandeur, et ses soirées circle pit, bagarre et bières, faites un
          don au groupe, vous ne serez pas déçu !</p>
      </div>
    </div>
    <a href="https://facebook.com/eightsins">
      <FacebookIcon class="icon" />
    </a>
  </main>
</template>

<style scoped lang="scss">
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 0 5px 1em;
  margin-bottom: 2em;
  box-shadow: rgba(0, 0, 0, 0.24) 0 3px 8px;

  #title {
    font-size: 1.6em;
  }

  @media (min-width: 768px) {
    padding-inline: 2.5em;

    #title {
      font-size: 2em;
    }
  }
}

main {
  padding: 0 15px;
  max-width: 1280px;
  margin: 0 auto;
}

.logo {
  @media (min-width: 768px) {
    width: 100px;
    right: 3em;
  }
}

.speech-container {
  max-width: 1080px;
  margin: 3em auto;

  @media (min-width: 768px) {
    display: flex;
  }

  #main-photo {
    border-radius: 12px;
    box-shadow: rgba(50, 50, 93, 0.25) 0 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
  }

  .speech {
    @media (min-width: 768px) {
      padding: 0 3em;
    }
  }
}

.icon {
  color: var(--secondary-color-main);
  font-size: 2.2em;
  transition: 100ms;

  &:hover {
    color: var(--secondary-color-light);
  }
}
</style>

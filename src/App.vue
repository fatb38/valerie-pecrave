<script setup lang="ts">
import FacebookIcon from '~icons/mdi/facebook'
import InstagramIcon from '~icons/mdi/instagram'
import TikTokIcon from '~icons/ic/baseline-tiktok'
import YoutubeIcon from '~icons/mdi/youtube'

const date = new Date()
</script>

<template>
  <header>
    <h1 id="title" class="secondary-color">Valérie Pecrave</h1>
    <img class="logo" src="/logo-valoche.jpg" alt="logo" width="90">
  </header>
  <main>
    <h2>Directrice de campagne officielle du groupe Eight Sins</h2>
    <h2 class="primary-color">En appel à votre générosité</h2>

    <a href="https://www.kisskissbankbank.com/fr/projects/eightsins">
      <button class="button primary">FAIRE UN DON</button>
    </a>

    <div class="speech-container">
      <div class="media-container">
        <video
          src="/speech-valerie.mp4"
          class="main-media"
          playsinline
          controls
        />
      </div>
      <div class="speech">
        <p class="bold">Le groupe <a href="https://eightsins.fr" class="primary-color bold">Eight Sins</a> a besoin de
          vous aujourd'hui pour
          boucler le budget de financement de son
          nouvel album.</p>
        <p class="bold">Valoche et toute son équipe de campagne font appel à vous, cher public, pour aider le groupe à
          apporter une nouvelle fraicheur <span class="primary-color">Thrash Metal</span> dans cette scène tant
          malmenée
          depuis la Covid Party
          2020-2021.</p>
        <p class="bold">Pour que la France retrouve sa grandeur, et ses soirées circle pit, bagarre et bières, faites
          un
          don au groupe, vous ne serez pas déçu !</p>
        <div class="link-icons">
          <div>
            <div>Suivez nous sur les réseaux sociaux</div>
            <a href="https://facebook.com/eightsins">
              <FacebookIcon class="icon facebook-icon-color" />
            </a>
            <a href="https://instagram.com/eightsinshxc">
              <InstagramIcon class="icon instagram-icon-color" />
            </a>
            <a href="https://youtube.com/eightsins">
              <YoutubeIcon class="icon youtube-icon-color" />
            </a>
            <a href="https://tiktok.com/@eightsinshxc">
              <TikTokIcon class="icon tiktok-icon-color" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </main>
  <footer>
    <div>Eight Sins {{ date.getFullYear() }} ©</div>
  </footer>
</template>

<style scoped lang="scss">
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 0 5px 1em;
  margin-bottom: 2em;
  box-shadow: rgba(0, 0, 0, 0.24) 0 3px 8px;
  font-family: 'Dancing Script', cursive;
  background-color: #fff;

  #title {
    font-size: 2.5em;
    margin: 0;
  }

  @media (min-width: 768px) {
    padding-inline: 2.5em;

    #title {
      font-size: 3em;
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

.button.primary {
  background-color: var(--primary-color-main);
  color: white;
  border-color: var(--primary-color-main);
  margin-top: 10px;

  &:hover {
    background-color: var(--primary-color-dark);
  }
}

.speech-link {
  display: flex;
  justify-content: center;

  .button {
    display: flex;
    align-items: center;
    justify-content: center;

    .speech-icon {
      margin-right: 10px;
      font-size: 18px;
      color: var(--secondary-color-main);
    }
  }
}


.speech-container {
  max-width: 1080px;
  margin: 35px auto;

  @media (min-width: 768px) {
    display: flex;
  }

  .media-container {
    .main-media {
      max-width: 100%;
      border-radius: 12px;
      box-shadow: rgba(50, 50, 93, 0.25) 0 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;

      @media (min-width: 768px) {
        margin-right: 30px;
      }

      @media (max-width: 768px) {
        video {
          max-width: 100%;
        }
      }
    }
  }

  .speech {
    display: flex;
    flex-direction: column;

    .link-icons {
      display: flex;
      place-items: center;
      flex-grow: 1;
      margin: 0 auto;
    }

    @media (min-width: 768px) {
      padding: 1em 3em;
      width: 70%;
    }
  }
}

.icon {
  font-size: 2.2em;
  transition: 100ms;
  margin: 0.3em;
  filter: grayscale(1);
  color: grey;

  &:hover {
    filter: grayscale(0);
  }
}

footer {
  margin-top: 10px;
  padding-top: 10px;
  padding-bottom: 5px;

  div {
    font-size: 14px;
    font-style: italic;
  }
}
</style>

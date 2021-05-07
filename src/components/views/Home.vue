<template>
  <div class="homepage">
    <div id="myHEADER">
      <div class="flex" id="header">
        <div class="flex" id="UX1">
          <div class="headerbutton" @click="smoothScroll('.homepage')">
            Home
          </div>
          <div class="headerbutton" @click="smoothScroll('.about')">
            About
          </div>
        </div>

        <div>
          <img id="Logo" src="../assets/Micolash.png" alt="" />
        </div>

        <div class="flex" id="UX2">
          <div class="headerbutton" @click="smoothScroll('.proj')">
            Projects
          </div>
          <div class="headerbutton" @click="smoothScroll('.cin')">Cinema</div>
        </div>
      </div>
    </div>
    <div id="home">
      <div></div>
      <hr class="hr about" />
      <div id="about"><h2>About</h2></div>
      <div class="flex" id="About">
        <div class="MitFoto">
          <img src="../assets/Ikkemig.jpg" alt="" />
        </div>

        <div class="AboutText">
          <div>
            <h1>Welcome to my portfolio</h1>
            <p>
              Spild af tid og pis mig i øret hvor lidt jeg gider at stå op til
              en så ligegyldig hverdag som er fucking kodning. Personer der
              føler kodning er vejen frem i livet har besynderligt lidt indhold
              i deres ellers så sprægfyldte hverdag. Folk der elsker kodning
              skulle have deres hverdag omlagt så de kunne rende rundt med deres
              meta tags og divvernivver, og babbe gren på det første individ der
              udstøder "MEDIA QUERIES". Her er min portfolio. Læs så meget af
              den du vil. Jeg har valgt at laveden baseret på fansites som
              sprang ud i de tidlige dage a internettet. Det skulle gerne bringe
              en nostalgi frem i folk, der samtidig griner af de forskellige
              billeder og tekster som jeg inkludere. NU hvor du har fået en
              introduktion til hvem jeg er, så fuck jer, fuck jeres opgaver og
              fuck hele det "curriculum" som i ikke laver andet end at følge
              blind som fucking aber.
            </p>
          </div>
        </div>
      </div>
      <hr class="hr proj" />
      <div class="Projects"><h2>Projects</h2></div>
      <div id="Projects">
        <v-carousel id="slideshow">
          <v-carousel-item
            v-for="(item, i) in items"
            :key="i"
            :src="item.src"
            reverse-transition="fade-transition"
            transition="fade-transition"
          ></v-carousel-item>
        </v-carousel>
        <!--    <img src="../assets/AlbumCover.png" alt="" />
      <img src="../assets/IdeaHouse.png" alt="" />
      <img src="../assets/MiniMe.png" alt="" />
      <img src="../assets/MuseumLogo.png" alt="" />
      <img src="../assets/Shapes.png" alt="" /> -->
      </div>
      <div class="gridbox">
        <div class="item">
          <img
            src="@/assets/holm assets/bcardfront.png"
            height="100%"
            width="100%"
          />
        </div>
        <div class="item">
          <img
            src="@/assets/holm assets/bcardback.png"
            height="100%"
            width="100%"
          />
        </div>
        <div class="item">
          <img
            src="@/assets/holm assets/highholm.png"
            height="100%"
            width="100%"
          />
        </div>
        <div class="item">
          <img
            src="@/assets/holm assets/ideaholm.png"
            height="100%"
            width="100%"
          />
        </div>
        <div class="item">
          <img
            src="@/assets/holm assets/treeholm.png"
            height="100%"
            width="100%"
          />
        </div>
        <div class="item">
          <img
            src="@/assets/holm assets/miniholm.png"
            height="100%"
            width="100%"
          />
        </div>
        <div class="item">
          <img
            src="@/assets/holm assets/awooo.png"
            height="100%"
            width="100%"
          />
        </div>
        <div class="item">
          <img
            src="@/assets/holm assets/abstract.png"
            height="100%"
            width="100%"
          />
        </div>
      </div>
      <hr class="hr cin" />

      <div class="Cinema">
        <h2>Cinema</h2>

        <div class="Video1">
          <iframe
            width="560"
            height="315"
            src="https://www.youtube.com/embed/Ho4e1fCkjB0"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>

        <div class="Video2">
          <iframe
            width="560"
            height="315"
            src="https://www.youtube.com/embed/CssOKCwT9Qo"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { gsap } from "gsap";
import { ScrollToPlugin } from "gsap/ScrollToPlugin";
gsap.registerPlugin(ScrollToPlugin);

export default {
  data() {
    return {
      items: [
        {
          src: require("../assets/holm assets/bcardfront.png"),
        },
        {
          src: require("../assets/holm assets/highholm.png"),
        },
        {
          src: require("../assets/holm assets/bcardback.png"),
        },
        {
          src: require("../assets/holm assets/ideaholm.png"),
        },
        {
          src: require("../assets/holm assets/treeholm.png"),
        },
        {
          src: require("../assets/holm assets/miniholm.png"),
        },
        {
          src: require("../assets/holm assets/awooo.png"),
        },
        {
          src: require("../assets/holm assets/abstract.png"),
        },
      ],
    };
  },
  methods: {
    smoothScroll(el) {
      gsap.to(window, {
        duration: 1,
        scrollTo: { y: el, offsetY: 0 },
        ease: "power2",
      });
    },
  },
};
</script>

<style lang="scss">
@import "./src/styles/variables.scss";
#myHEADER {
  position: fixed;
  z-index: 5;
  border-bottom: 2px solid black;
  border-radius: 0 0 10px 10px;
  width: 100%;
  height: 120px;
  background-color: map-get($Colorscheme, Tertiary);
  .flex {
    display: flex;
    justify-content: space-around;
  }

  #Logo {
    border: 2px solid black;
    border-radius: 0 0 5px 5px;
    position: absolute;
    z-index: 3;
    margin-left: auto;
    margin-right: auto;
    left: 0;
    right: 0;
    text-align: center;
  }

  #header {
    border-bottom: 5px solid black;
    border-radius: 0 0 10px 10px;
    overflow: hidden;
    width: 100%;
    height: 120px;
    background: linear-gradient(
      map-get($Colorscheme, Tertiary),
      map-get($Colorscheme, Primary)
    );
  }

  #UX1,
  #UX2 {
    width: 25%;
    margin-top: 5%;
    @media (max-width: 715px) {
      display: none;
    }
    @media (min-width: 715px) {
      margin-top: 20px;
    }
  }
}

#home {
  margin-top: 180px;
}
#about {
    margin: 200px auto 40px auto;
}
#About {
  margin: 40px auto;
  padding: 20px 30px;
  img {
    border: 2px solid black;
    border-radius: 5px;
  }
  @media (max-width: 500px) {
    flex-direction: column;
  }
}
.AboutText {
  padding: 0 20px;
}

.flex {
  display: flex;
  justify-content: space-around;
}
.Video1 {
  overflow: hidden;
  /* 16:9 aspect ratio */
  padding-top: 56.25%;
  position: relative;
}
.Video1 iframe {
  border: 0;
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 100%;
}
.Video2 {
  overflow: hidden;
  /* 16:9 aspect ratio */
  padding-top: 56.25%;
  position: relative;
}
.Video2 iframe {
  border: 0;
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 100%;
}

.Projects {
  margin: 200px auto 40px auto;
  height: 20px;
  img {
    height: 100%;
    width: auto;
  }
}
#Projects {
  max-height: 700px;
  padding: 20px 30px;

  #slideshow {
    margin: 40px auto;
    border-radius: 27% 87% 13% 80% / 77% 24% 99% 17%;
    border: 2px solid black;
  }
}
.Cinema {
  margin: 200px auto 40px auto;
}
.Video1,
.Video2 {
  margin: 40px 30px;
  border-radius: 77% 24% 99% 17% / 27% 87% 13% 80%;
}

.gridbox {
  display: grid;
  grid-template-columns: auto auto auto auto;
  height: auto;
  margin: 1rem 4rem 1rem 4rem;
  gap: 1rem;

  .item {
    box-shadow: rgba(3, 8, 20, 0.1) 0px 0.15rem 0.5rem,
      rgba(2, 8, 20, 0.1) 0px 0.075rem 0.175rem;
  }
}
</style>
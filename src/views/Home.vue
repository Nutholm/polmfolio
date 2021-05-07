<template>
  <div class="homepage">
    <div id="myHEADER">
      <div class="flex" id="header">
        <div class="flex" id="UX1">
          <div class="headerbutton" @click="smoothScroll('.homepage')">
            Home
          </div>
          <div class="headerbutton" @click="smoothScroll('.about')">About</div>
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
      <hr class="hr" />
      <h3 style="color: white; margin: 15px 0">
        Come on then, take a sit. We can watch life pass on by...
      </h3>
      <div id="gif">
        <img
          height="500"
          width="500"
          src="https://media1.tenor.com/images/c805c00fc361edd711942c81cb8ce39e/tenor.gif"
          alt=""
        />
      </div>
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
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus
              pharetra vestibulum dictum. Donec feugiat scelerisque turpis, ac
              fringilla magna semper eu. Nullam ornare tellus ac tincidunt
              suscipit. Curabitur molestie est id justo rutrum, nec luctus elit
              suscipit. Etiam auctor urna quis scelerisque posuere. Donec
              bibendum sem non nibh viverra, vitae imperdiet ipsum semper. Proin
              suscipit augue purus, in elementum arcu fermentum convallis.
              Pellentesque in nisi vitae risus condimentum ullamcorper. Duis
              posuere magna eu enim cursus, non finibus urna molestie. Donec
              tempor augue ac sollicitudin semper. Pellentesque eu justo id nisl
              blandit condimentum. Praesent congue arcu sed nunc vehicula
              ullamcorper. Pellentesque enim metus, rutrum in volutpat a,
              gravida quis velit. In hac habitasse platea dictumst. Vivamus
              neque sapien, semper in dictum non, semper nec ipsum.
              <!-- Spild af tid og pis mig i øret hvor lidt jeg gider at stå op til
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
              blind som fucking aber. -->
            </p>
          </div>
        </div>
      </div>
      <hr class="hr proj" />
      <div class="Projects"><h2>Projects</h2></div>
      <p style="margin-top: 70px; margin-bottom: -30px">
        My Artworks presented in a humble slideshow...
      </p>

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
      <p style="margin-bottom: 20px">
        Right click and open in a new tab, should you want to examine further...
      </p>

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
        <h3 style="margin-top: -30px; margin-bottom: 20px">Video CV</h3>
        <p style="margin-bottom: 130px">This project was about...</p>

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
        <h3 style="margin-top: -30px; margin-bottom: 20px">Promo Commercial</h3>
        <p style="margin-bottom: 130px">This project was about...</p>

        <div class="Video3">
          <iframe
            width="560"
            height="315"
            src="https://www.youtube.com/embed/FmBXdCh3oWw"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>
        <h3 style="margin-top: -30px; margin-bottom: 20px">Short Movie</h3>
        <p style="margin-bottom: 130px">This project was about...</p>
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
#gif {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  overflow: hidden;
  width: 400px;
  height: 400px;
  border-radius: 20% 80% 20% 80% / 80% 20% 80% 20%;
  border: 2px solid black;
}
.item {
  border: 2px solid black;
}
h2 {
  font-size: 50px;
  color: white;
  -webkit-text-stroke: 3px solid black;
  font-family: "Goblin One", cursive;
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
  @media (max-width: 800px) {
    flex-direction: column;
  }
  @media (min-width: 1200px) {
    padding: 20px 200px;
  }
}
.AboutText {
  padding: 0 20px;
  background: linear-gradient(rgba(255, 255, 255, 0.397), rgba(0, 0, 0, 0));
  border-radius: 10px;
  @media (min-width: 1000px) {
    background: linear-gradient(rgba(255, 255, 255, 0.397), rgba(0, 0, 0, 0));
    border: 10px;
    margin: 0 75px;
    font-weight: 500;
  }
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
.Video3 {
  overflow: hidden;
  /* 16:9 aspect ratio */
  padding-top: 56.25%;
  position: relative;
}
.Video3 iframe {
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
  @media (min-width: 900px) {
    padding: 20px 120px;
  }
  @media (min-width: 1200px) {
    padding: 20px 250px;
  }
  #slideshow {
    margin: 40px auto;
    border-radius: 27% 87% 13% 80% / 77% 24% 99% 17%;
    border: 2px solid black;
  }
}
.Cinema {
  margin: 200px auto 40px auto;
  @media (min-width: 900px) {
    padding: 20px 120px;
  }
  @media (min-width: 1200px) {
    padding: 20px 250px;
  }
}
.Video1 {
  margin: 40px 30px;
  border-radius: 27% 87% 13% 80% / 27% 24% 19% 27%;
  border: 2px solid black;
}
.Video2 {
  margin: 40px 30px;
  border-radius: 77% 17% 57% 9% / 14% 49% 13% 90%;
  border: 2px solid black;
}
.Video3 {
  margin: 40px 30px;
  border-radius: 77% 24% 99% 17% / 27% 87% 13% 80%;
  border: 2px solid black;
}

.gridbox {
  display: grid;
  @media (min-width: 900px) {
    padding: 20px 300px;
  }
  grid-template-columns: auto auto auto auto;
  height: auto;
  margin: 1rem 4rem 1rem 4rem;
  gap: 1rem;

  .item {
    box-shadow: rgba(3, 8, 20, 0.1) 0px 0.15rem 0.5rem,
      rgba(2, 8, 20, 0.1) 0px 0.075rem 0.175rem;
  }
  .item:nth-child(1) {
    animation: appear 0.3s ease-out;
  }
  .item:nth-child(2) {
    animation: appear 0.5s ease-out;
  }
  .item:nth-child(3) {
    animation: appear 0.7s ease-out;
  }
  .item:nth-child(4) {
    animation: appear 0.9s ease-out;
  }
  .item:nth-child(5) {
    animation: appear 1.1s ease-out;
  }
  .item:nth-child(6) {
    animation: appear 1.3s ease-out;
  }
  .item:nth-child(7) {
    animation: appear 1.5s ease-out;
  }
  .item:nth-child(8) {
    animation: appear 1.7s ease-out;
  }
}
</style>
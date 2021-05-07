<template>
  <div class="homepage">
    <hr class="hr" />
    <div class="flex" id="About">
      <div class="MitFoto">
        <img src="../assets/Ikkemig.jpg" alt="" />
      </div>

      <div class="AboutText">
        <div>
          <h1>Welcome to my portfolio</h1>
          <p>
            Spild af tid og pis mig i øret hvor lidt jeg gider at stå op til en
            så ligegyldig hverdag som er fucking kodning. Personer der føler
            kodning er vejen frem i livet har besynderligt lidt indhold i deres
            ellers så sprægfyldte hverdag. Folk der elsker kodning skulle have
            deres hverdag omlagt så de kunne rende rundt med deres meta tags og
            divvernivver, og babbe gren på det første individ der udstøder
            "MEDIA QUERIES". Her er min portfolio. Læs så meget af den du vil.
            Jeg har valgt at laveden baseret på fansites som sprang ud i de
            tidlige dage a internettet. Det skulle gerne bringe en nostalgi frem
            i folk, der samtidig griner af de forskellige billeder og tekster
            som jeg inkludere. NU hvor du har fået en introduktion til hvem jeg
            er, så fuck jer, fuck jeres opgaver og fuck hele det "curriculum"
            som i ikke laver andet end at følge blind som fucking aber.
          </p>
        </div>
      </div>
      
    </div>
<hr class="hr" />
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
    <hr class="hr" />

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
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg",
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg",
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg",
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./src/styles/variables.scss";
.home {
  height: 200vh;
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

    border: 1px solid black;
  }
}

.Video1, .Video2 {
    margin: 40px 30px;

}
</style>
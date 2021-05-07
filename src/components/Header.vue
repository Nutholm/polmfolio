<template>
  <div>
    <div class="flex" id="header">
      <div class="flex" id="UX1">
        <div>Home</div>
        <div>About</div>
      </div>

      <div>
        <img id="Logo" src="../assets/Micolash.png" alt="" />
      </div>

      <div class="flex" id="UX2">
        <div>Projects</div>
        <div>Cinema</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../styles/variables.scss";

.flex {
  display: flex;
  justify-content: space-around;
}

#Logo {
  border: 2px solid black;
  border-radius: 0 0 5px 5px;
  position: absolute;
  margin-left: auto;
  margin-right: auto;
  left: 0;
  right: 0;
  text-align: center;
}

#header {
  border-bottom: 2px solid map-get($Colorscheme, Tertiary);
  border-radius: 0 0 10px 10px;
  overflow: hidden;
  width: 100%;
  height: 120px;
  background-color: map-get($Colorscheme, Tertiary);
}

#UX1,
#UX2 {
  width: 25%;
  margin-top: 5%;
  @media (max-width: 715px) {
    display: none;
  }
}
</style>
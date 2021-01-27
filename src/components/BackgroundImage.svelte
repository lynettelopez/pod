<script>
  let tabletPath = "./static/images/host-tablet.jpg";
  let desktopPath = "./static/images/host-desktop.jpg";

  export let screenWidth;
</script>

{#if screenWidth < 700}
  <div class="background" />
{:else if screenWidth >= 700 && screenWidth < 1120}
  <img src={tabletPath} alt="Man speaking into a microphone" />
{:else if screenWidth >= 1120}
  <img src={desktopPath} alt="Man speaking into a microphone" />
{/if}

<style lang="scss">
  @import "../styles/theme.scss";

  .background {
    height: 100%;
    background-image: url(../static/images/host-mobile.jpg);
    background-size: cover;
    mix-blend-mode: screen;
    opacity: 0.1;
  }

  img {
    position: absolute;
    top: 0;
    right: 0;

    @include responsive(desktop) {
      top: 8.125em;
    }
  }
</style>

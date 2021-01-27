<script>
  import BackgroundImage from "./components/BackgroundImage.svelte";
  import Logo from "./components/Logo.svelte";
  import PageContent from "./components/PageContent.svelte";
  import Pattern from "./components/Pattern.svelte";

  let width;
</script>

<main bind:clientWidth={width}>
  <Logo />
  <BackgroundImage screenWidth={width} />
  <PageContent screenWidth={width} />
  <Pattern />
</main>

<style lang="scss">
  @import "./styles/theme.scss";

  main {
    height: 100vh;
    position: relative;
    overflow-x: hidden;
    background-color: $background;
  }
</style>

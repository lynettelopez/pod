<script>
  let path = "./static/svgs/logo.svg";
</script>

<a href="/"><img src={path} alt="Pod logo" /></a>

<style lang="scss">
  @import "../styles/theme.scss";

  img {
    position: absolute;
    top: 10%;
    left: 50%;
    transform: translate(-50%, -10%);

    @include responsive(tablet) {
      top: 5%;
      left: 5%;
      transform: translate(-5%, -5%);
    }

    @include responsive(desktop) {
      top: 11.33%;
      left: 11.5%;
      transform: translate(-11.5%, -11.33%);
    }
  }
</style>

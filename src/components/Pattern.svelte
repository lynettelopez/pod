<script>
  let path = "./static/svgs/bg-pattern-dots.svg";
</script>

<img src={path} alt="Rows of teal dots" />

<style lang="scss">
  @import "../styles/theme.scss";

  img {
    display: none;

    @include responsive(tablet) {
      display: block;
      position: absolute;
      bottom: 0;
      left: 5%;
    }

    @include responsive(desktop) {
      bottom: 4.875em;
      left: 84%;
    }
  }
</style>

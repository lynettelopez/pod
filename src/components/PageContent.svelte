<script>
  import Form from "./Form.svelte";

  export let screenWidth;
</script>

<div class="page-content">
  <h1><span>Publish your podcasts</span> everywhere.</h1>
  <p>
    Upload your audio to Pod with a single click. We’ll then distribute your
    podcast to Spotify, Apple Podcasts, Google Podcasts, Pocket Casts and more!
  </p>
  {#if screenWidth < 700}
    <div class="podcast-logos">
      <img src="./static/svgs/spotify.svg" alt="Spotify logo" />
      <img src="./static/svgs/apple-podcast.svg" alt="Apple Podcast logo" />
      <img src="./static/svgs/google-podcasts.svg" alt="Google Podcasts logo" />
      <img src="./static/svgs/pocket-casts.svg" alt="Pocket Casts logo" />
    </div>
    <Form {screenWidth} />
  {:else}
    <Form {screenWidth} />
    <div class="podcast-logos">
      <img src="./static/svgs/spotify.svg" alt="Spotify logo" />
      <img src="./static/svgs/apple-podcast.svg" alt="Apple Podcast logo" />
      <img src="./static/svgs/google-podcasts.svg" alt="Google Podcasts logo" />
      <img src="./static/svgs/pocket-casts.svg" alt="Pocket Casts logo" />
    </div>
  {/if}
</div>

<style lang="scss">
  @import "../styles/theme.scss";

  .page-content {
    width: 87%;
    position: absolute;
    top: 26.5%;
    left: 50%;
    transform: translateX(-50%);
    text-align: center;
    font-family: $chivo;

    @include responsive(tablet) {
      width: 83%;
      top: 25%;
      left: 5%;
      padding-bottom: 5%;
      transform: none;
      text-align: left;
      background-color: $background;
    }

    @include responsive(desktop) {
      width: 50.2%;
      top: 29%;
      left: 11.5%;
    }

    h1 {
      font-weight: $light;
      text-transform: uppercase;
      font-size: 1.625em;
      line-height: 2.375rem;
      color: $white;

      @include responsive(tablet) {
        font-size: 3em;
        line-height: 3.5rem;
        margin-top: 5.8125rem;
      }

      @include responsive(desktop) {
        font-size: 3.25em;
        line-height: 3.875rem;
        margin-top: 5.5rem;
      }

      span {
        color: $accent;
      }
    }

    p {
      font-size: 0.9375em;
      line-height: 1.5625rem;
      margin-top: 1rem;
      color: $tertiary;

      @include responsive(tablet) {
        width: 70%;
        font-size: 1.125em;
        line-height: 1.75rem;
        margin-top: 1.9375rem;
      }

      @include responsive(desktop) {
        width: 61.5%;
        margin-top: 1.5rem;
      }
    }

    .podcast-logos {
      width: 19.5625em;
      margin: 2.0625em auto 0;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;

      @include responsive(tablet) {
        width: 33.5em;
        height: 1.8125em;
        margin: 4em 0 0 0;
      }

      img:nth-child(1) {
        width: 3.49625em;

        @include responsive(tablet) {
          width: 6em;
        }
      }

      img:nth-child(2) {
        width: 2.8125em;

        @include responsive(tablet) {
          width: 4.875em;
        }
      }

      img:nth-child(3) {
        width: 4.5625em;

        @include responsive(tablet) {
          width: 7.8125em;
        }
      }

      img:nth-child(4) {
        width: 4.7425em;

        @include responsive(tablet) {
          width: 8.0625em;
        }
      }
    }
  }
</style>

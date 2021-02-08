<script>
  export let screenWidth;
</script>

<form>
  <label for="email">Email address</label>
  <input id="email" type="email" placeholder="Email address" required />
  {#if screenWidth >= 1120}
    <span>Oops! Please check your email</span>
  {/if}
  <button type="submit">Request Access</button>
</form>

<style lang="scss">
  @import "../styles/theme.scss";

  form {
    display: flex;
    flex-direction: column;
    margin-top: 3em;
    font-weight: $bold;
    font-size: 0.875em;
    line-height: 1.75rem;

    & > * {
      border-radius: 50px;
      border-style: none;
    }

    // Hides the label while still making it accessible to screen readers
    label[for="email"] {
      border: 0;
      clip: rect(0 0 0 0);
      height: 1px;
      margin: -1px;
      overflow: hidden;
      padding: 0;
      position: absolute;
      width: 1px;
    }

    input {
      height: 2.875rem;
      background-color: $primary;
      color: $white;
      padding-left: 2em;
      z-index: 1;

      @include responsive(tablet) {
        width: 26.6875rem;
        height: 3.5rem;
      }
    }

    span {
      visibility: hidden;
      position: relative;
      top: -2rem;
      left: 2rem;
      color: $error;
      font-size: 0.75em;
      line-height: 0.875rem;
      transition: all 0.4s;
      z-index: 0;
    }

    @include responsive(desktop) {
      input:focus:invalid + span {
        visibility: visible;
        top: 0.5rem;
      }
    }

    button {
      height: 2.875rem;
      background-color: $accent;
      color: $background;
      margin: 1rem 0 3.875rem 0;
      transition: all 0.2s;
      z-index: 2;

      @include responsive(tablet) {
        position: absolute;
        width: 10.125rem;
        height: 2.875rem;
        margin: 0.3125rem 0.3125rem 0.3125rem 16.25rem;
      }

      @include responsive(desktop) {
        &:hover {
          background-color: $accent-light;
        }
      }
    }

    input:focus,
    button:focus {
      outline: none;
    }
  }
</style>

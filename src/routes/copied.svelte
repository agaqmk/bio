<script lang="ts">
  import Link from '../lib/Link.svelte';
</script>

<div class="cont">
  <div class="inlineme pct">
    <div>
      <div class="inlineme profilething">
        <img
          src="https://cdn.discordapp.com/avatars/898971210531078164/0d5b68065a4027f81586b8bcd18cd95a.webp?size=4096"
          alt=""
          class="inlineme left"
        />
        <div class="inlineme right">
          <p>Yielding</p>
        </div>
      </div>
      <hr />
      <p>
        Developer, Penetration Tester<br />
        <Link to="/">Back</Link>
      </p>
    </div>
    My Discord has been copied to your clipboard.<br />
    Incase it hasn't, you can do one of the following:
    <ul>
      <li>Manually Type it: Yielding#3961</li>
      <li>
        <a
          href="https://cord.breadhub.cc/"
          target="_blank"
          rel="noopener noreferrer">Join the Bread Hub Discord</a
        >
      </li>
    </ul>
  </div>
</div>

<style lang="scss">
  @use '../macchiato';
  .inlineme {
    display: inline-block;
  }
  .profilething {
    font-size: 2em;
    align-items: center;
    justify-content: center;
    display: flex;
    img {
      height: 1em;
    }
    .right {
      text-align: left;
      height: 100%;
      margin-left: 1rem;
    }
  }
  .cont {
    margin: 16px 16px;

    img {
      height: 80px;
    }
  }
</style>

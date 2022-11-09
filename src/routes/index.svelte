<script lang="ts">
  import Link from '../lib/Link.svelte';
  import { discord, name, pfp, smolabt } from '../me';
</script>

<div class="cont">
  <div class="inlineme pct">
    <div>
      <div class="inlineme profilething">
        <img src={pfp} alt="" class="inlineme left" />
        <div class="inlineme right">
          <p>{name}</p>
        </div>
      </div>
      <hr />
      <p>
        {smolabt}
        <br />
        <Link to="/about">About</Link><br />
        <Link to="/projects">Projects</Link>
      </p>
    </div>
    <div>
      Contact Me:<br />
      <Link to="/mastodoninstances">Mastodon</Link><br />
      <Link
        to="/copied"
        on:click={() => {
          navigator.clipboard.writeText(discord);
          return '/copied';
        }}
      >
        Discord
      </Link><br />
      <Link to="/github">Github</Link>
    </div>
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

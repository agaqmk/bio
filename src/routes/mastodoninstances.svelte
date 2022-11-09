<script lang="ts">
  import Link from '../lib/Link.svelte';
  import { name, pfp, smolabt } from '../me';
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
        {smolabt}<br />
        <Link to="/">Back</Link>
      </p>
    </div>
    <div class="projl">
      <h2>Mastodon</h2>
      <div style="color: #dedede; overflow-y: auto; max-height: 50vh;">
        <p>
          <a
            href="https://p.astolfo.gay/@penguin"
            target="_blank"
            rel="noopener noreferrer"
            ><span class="l">@penguin</span>@p.astolfo.gay</a
          >
          | Shitposting, General stuff
          <br />
          <a
            href="https://p.astolfo.gay/@aga@fosstodon.org"
            target="_blank"
            rel="noopener noreferrer"
            ><span class="l">@aga</span>@fosstodon.org</a
          >
          | FOSS Projects
          <br />
        </p>
      </div>
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
  .projl {
    .l {
      color: #564fa3;
    }
  }
</style>

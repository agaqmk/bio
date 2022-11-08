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
    <div class="projl">
      <h2>Mastodon</h2>
      <div style="color: #dedede; overflow-y: auto; max-height: 50vh;">
        <p>
          <a
            href="https://p.astolfo.gay/@Yielding"
            target="_blank"
            rel="noopener noreferrer"
            ><span class="l">@Yielding</span>@p.astolfo.gay</a
          >
          | Shitposting
          <br />
          <a
            href="https://p.astolfo.gay/@yielding@fosstodon.org"
            target="_blank"
            rel="noopener noreferrer"
            ><span class="l">@yielding</span>@fosstodon.org</a
          >
          | FOSS Projects
          <br />
          <a
            href="https://p.astolfo.gay/@yielding@a.sc"
            target="_blank"
            rel="noopener noreferrer"><span class="l">@yielding</span>@a.sc</a
          >
          | General Projects
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

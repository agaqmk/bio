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
    <div
      class="okthisisthelikemaincontentthingyeahithinkyouunderstandwhatimeanwiththat"
    >
      <h2>About Me</h2>
      <p style="color: #dedede">
        Hi! I'm Yielding, a 15 year old full-stack developer from Switzerland.<br
        />
        <!-- start: i simply bypass -->
        I spend most of my free time discovering exploits for games.<br /><br />
        <!-- end: i simply bypass -->
        Overall, I'm a pretty chill person.<br />
        <em
          >I honestly don't quite know what to put here.<br />I'll likely put
          something here eventually.</em
        >
      </p>
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
  @media screen and (min-width: 1500px) {
    .okthisisthelikemaincontentthingyeahithinkyouunderstandwhatimeanwiththat {
      max-width: 35vw;
    }
  }
</style>

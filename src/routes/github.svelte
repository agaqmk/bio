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
    <h2>Github</h2>
    <a href="https://github.com/YieldingExploiter">Click Here</a> to go to my
    github.<br /><br />
    This page is <a href="https://github.com/YieldingExploiter/bio">FOSS</a>!<br
    />
    (License: <Link to="/agpl">AGPL</Link>)
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

<script lang="ts">
  import Link from '../lib/Link.svelte';
  import { discord, name, pfp, smolabt } from '../me';
</script>

<div class="cont">
  <div class="inlineme pct">
    <div>
      <div class="inlineme profilething">
        <img src={pfp} alt="pf" class="inlineme left" />
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
    My Discord has been copied to your clipboard.<br />
    Incase it hasn't, you can do one of the following:
    <ul>
      <li>Manually Type it: {discord}</li>
      <li>
        <a
          href="https://discord.gg/rmDdrgcV"
          target="_blank"
          rel="noopener noreferrer">Join my Discord!!!!</a
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

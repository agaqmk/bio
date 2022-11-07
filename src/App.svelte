<script lang="ts">
  // imported routes
  import index from './routes/index.svelte';
  import Copied from './routes/copied.svelte';

  // get base route
  import { baseRoute } from './BaseRoute';

  // route list - include leading /
  const Routes: Record<string, any> = {
    '/copied': Copied,
    '/about': About,
    '/projects': Projects,
    '/github': Github,
    '/mastodoninstances': MastodonInstances,
    '/': index, // index should be last!
  };

  // routing + whatnot
  import { Router, Route } from 'svelte-routing';
  import GenshinSound from './lib/GenshinSound.svelte';
  import About from './routes/about.svelte';
  import Projects from './routes/projects.svelte';
  import Github from './routes/github.svelte';
  import MastodonInstances from './routes/mastodoninstances.svelte';
  export let url = '';
</script>

<Router {url}>
  <div class="lecontent">
    <div class="lecontainer">
      {#each Object.entries(Routes) as [path, Page]}
        <Route path={`${baseRoute}${path}`}><Page /></Route>
        <Route path={`${path}`}><Page /></Route>
      {/each}
    </div>
  </div>
</Router>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div
  class="loadoverlay"
  on:click={() => {
    document.querySelector('.loadoverlay').classList.add('byebye');
    // @ts-ignore
    document.querySelectorAll('[data-autoplay]').forEach((v) => v.play());
  }}
>
  <h2>Click anywhere</h2>
</div>
<GenshinSound />

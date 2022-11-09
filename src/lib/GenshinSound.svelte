<!-- mute button when :troll: -->
<script lang="ts">
  import baseRoute from '../BaseRoute';

  const sounds = [
    '/clair-de-lune.mp3',
    '/un-sospiro.mp3'
  ].map((v) => `${baseRoute}${v}`);
  const getRandomSound = () =>
    sounds[Math.floor(Math.random() * sounds.length)];
  let sound = sounds[0];
  setInterval(() => {
    const el = document.querySelector('[data-genshin-ost]') as HTMLAudioElement;
    el.volume = 0.1;
  }, 500);
</script>

<audio
  src={sound}
  on:ended={() => {
    sound = getRandomSound();
    // @ts-ignore
    document.querySelector('[data-genshin-ost]').src = sound;
    // @ts-ignore
    document.querySelector('[data-genshin-ost]').play();
  }}
  data-autoplay
  data-genshin-ost
/>

<!-- mute button when :troll: -->
<script lang="ts">
  const sounds = [
    '/GenshinOST/Genshin-Impact-Main-Theme-原神192.ogg',
    '/GenshinOST/A-Day-in-Mondstadt-蒙德的一日.ogg',
    '/GenshinOST/Dream-Aria-_Genshin-Impact-Main-Theme-梦之咏叹.ogg',
    '/GenshinOST/The-City-Favored-By-Wind-风所爱之城.ogg',
    '/GenshinOST/Twilight-Serenity-_Genshin-Impact-Main-Theme-宁静的黄昏.ogg',
  ];
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

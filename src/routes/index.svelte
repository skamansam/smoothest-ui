<script lang="ts">
  import { onMount } from 'svelte';
  import App from '../lib/App.svelte';
  const appTitle = 'Smoothest UI';

  let themeMode = 'light';

  onMount(() => {
    if(typeof localStorage == `undefined`) return;
    if (localStorage.getItem('themeMode') === 'dark' || (!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
      themeMode = 'dark';
    }
  });
</script>

<style>
a, .fancy__underline span {
 display: inline-block;
 background-position-x: -100%;
 background-image: linear-gradient( transparent 50%, #67b3e8 50%);
 transition: background .3s ease;
 background-repeat: no-repeat;
 background-size: 100% 100%;
 text-decoration: none;
 font-weight: 600;
}
 a:hover, .fancy__underline span:hover {
    background-position-x: 100%;
 }
</style>

<App title={appTitle} themeMode={themeMode} class="{themeMode} h-screen">
  <h1>Welcome to {appTitle}</h1>
  <p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

  <div slot="footer" class="text-sm">
    <div class="col">
    Created with <i class="ri-heart-2-line"></i> by "Skamans Sam" Tyler<br/>
    Icons are <a href="https://remixicon.com/" class=""><i class="ri-remixicon-line ri-fw"></i> Remix</a>
    </div>
  </div>
</App>
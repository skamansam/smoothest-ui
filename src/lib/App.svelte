<script>
  import AppHeader from "./AppHeader.svelte";
  import AppFooter from "./AppFooter.svelte";
  import AppNav from "./AppNav.svelte";
  export let title = 'Default App Title';
  let clazz;
  export { clazz as class };
</script>

<div class="app {clazz} parent flex flex-col h-screen">
  <AppHeader title="{title}" class="bg-violet-500 p-4 text-left">
    <slot name="header"></slot>
  </AppHeader>
  <main class="flex-1 flex">
    <AppNav title="{title}" class="sidebar p-4 bg-violet-500 text-left w-16 md:w-32 lg:w-48 h-screen  hover:w-48 pt-16 transition-all">
      <slot name="nav"></slot>
    </AppNav>
    <section class="content flex-1 bg-slate-200 text-left p-4">
      <slot></slot>
    </section>
  </main>
  <AppFooter class="bg-indigo-500 p-4 min-h-24">
    <slot name="footer"></slot>
  </AppFooter>
</div>

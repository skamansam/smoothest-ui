<script>
  import AppHeader from "./AppHeader.svelte";
  import AppFooter from "./AppFooter.svelte";
  import AppNav from "./AppNav.svelte";
</script>

<AppHeader>
  <slot name="header"></slot>
</AppHeader>

<AppNav>
  <slot name="nav"></slot>
</AppNav>

<main>
  <slot></slot>
</main>

<AppFooter>
  <slot name="footer"></slot>
</AppFooter>
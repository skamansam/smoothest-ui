<script>
export let title='Default App';
let clazz;
export { clazz as class };
</script>

<header class="{clazz}">
  <div class="font-bold font-sans text-3xl self-center justify-self-center">
    <slot name="title">
      {title}
    </slot>
  </div>
</header>


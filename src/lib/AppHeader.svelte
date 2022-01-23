<script>
export let title='Default App';
</script>

<header class="absolute inset-x-0 top-0 h-16 bg-violet-500 flex">
  <div class="font-bold font-sans text-3xl self-center justify-self-center">
    <slot name="title">
      {title}
    </slot>
  </div>
</header>


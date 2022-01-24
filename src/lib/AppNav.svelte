
<script>
export let title='Navigation'
let clazz;
export { clazz as class };
</script>

<nav class="{clazz}">
  <slot name="header">
    <div>
      <i class="ri-home-fill"></i>
      <span class="ms:w-1">{title}</span>
    </div>
  </slot>
  
  <slot>

  </slot>
</nav>
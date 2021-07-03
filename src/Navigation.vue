<template>
  <header class="navigation">
    <nav>
      <ul>
        <slot></slot>
      </ul>
    </nav>
  </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue'


export default defineComponent({
  name: 'Navigation'
})
</script>

<style lang="scss" scoped>
.navigation  {
  width: 100%;
  height: 4.5rem;
  background: var(--bto-nav-bg, #41b883);
  
  nav {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
  }

  ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    height: 100%;
    justify-content: center;
    align-items: center;
  }
}
</style>
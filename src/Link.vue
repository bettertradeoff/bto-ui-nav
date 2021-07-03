<template>
  <li class="nav-item">
    <router-link :to="to">
      <slot></slot>
    </router-link>
  </li>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Link',
  props: [ 'to' ]
})
</script>

<style lang="scss" scoped>
.nav-item {
  margin: 0 1rem;
  border-radius: 5px;

  a {
    --color: white;
    --border-radius: 5px;
    --padding: 0.5rem 1rem;
  }
  &:hover {
    background: white;
    color: #00179b;
  }
  &:hover a {
    --color: black;
  }

  a {
    display: block;
    text-decoration: var(--text-decoration, none);
    color: var(--color, black);
    border-radius: var(--border-radius, 0);
    padding: var(--padding, 0);
    cursor: pointer;

    &.router-link-active {
      background: var(--background-active, white);
      color: var(--color-active, black);
      cursor: auto;
    }
  }
}
</style>
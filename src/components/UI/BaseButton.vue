<template>
<!-- <button.. is what it will be rendered by vue instead of base-button, so <base-button type="submit" == <button type="submit" -->
  <button :type="type" :class="mode">
    <slot></slot>
  </button>
</template>

<script>
export default {
  // 'type' is not really necessary, this because of the Vue behaviour (<base-button type="submit"> => <button type="submit">)
  // props: ['type', 'mode']
  props: ['mode']
}
</script>

<style scoped>
button {
  padding: 0.75rem 1.5rem;
  font-family: inherit;
  background-color: #3a0061;
  border: 1px solid #3a0061;
  color: white;
  cursor: pointer;
}

button:hover,
button:active {
  background-color: #270041;
  border-color: #270041;
}

.flat {
  background-color: transparent;
  color: #3a0061;
  border: none;
}

.flat:hover,
.flat:active {
  background-color: #edd2ff;
}
</style>
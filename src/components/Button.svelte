<script>
export let primary = false;
export let text = false;
export let small = false;
</script>

<button {...$$props} class={$$props.class} class:primary class:text class:small on:click>
  <slot />
</button>

<style>
button {
  padding: 1.2rem 2.4rem;
  border: none;
  border-radius: 8px;
  font-weight: 700;
  line-height: 2rem;
  background-color: var(--dimmed-300);
  cursor: pointer;
}

:global(body.fonts-loading) button {
  font-family: Helvetica;
  line-height: 1.3;
  letter-spacing: -0.3px;
}

button:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}

button.primary {
  background-color: var(--primary);
}

button.text {
  background: none;
}

button.small {
  padding: 6px 1.2rem;
  border-radius: 6px;
  font-size: 1.4rem;
  line-height: initial;
}
</style>

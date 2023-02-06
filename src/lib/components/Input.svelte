<script lang="ts">
  import type { HTMLInputAttributes } from "svelte/elements";

  export let label: string;
  export let cols: number | undefined = undefined;
  export let rows: number | undefined = undefined;

  interface $$Props extends HTMLInputAttributes {
    label: string;
    cols?: number;
    rows?: number;
  }

  const id = Math.random();
</script>

<div class="input-wrapper">
  <label for={id.toString()}>{label}</label>
  <svelte:element
    this={cols || rows ? "textarea" : "input"}
    {...$$restProps}
    type="text"
    {cols}
    {rows}
    id={id.toString()}
  />
</div>

<style>
  .input-wrapper {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }

  textarea {
    resize: vertical;
  }

  textarea,
  input {
    width: 100%;
    padding: 1rem;
    outline: transparent;
    border: 3px solid hsl(0, 0%, 97%);
    border-radius: var(--radius-400);
  }

  textarea:focus,
  input:focus {
    border-color: var(--clr-accent-400);
  }
</style>

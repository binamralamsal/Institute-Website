<script lang="ts">
  import type { HTMLButtonAttributes } from "svelte/elements";

  type Variant = "primary";

  export let href: string | undefined = undefined;
  export let variant: Variant = "primary";

  interface $$Props extends HTMLButtonAttributes {
    href?: string | undefined;
    variant?: Variant;
  }
</script>

<svelte:element
  this={href ? "a" : "button"}
  {...$$restProps}
  class:btn={true}
  class:primary={variant === "primary"}
  {href}
>
  <slot />
</svelte:element>

<style>
  .btn {
    background: none;
    border: none;
    text-decoration: none;
    padding: 0.75em 1.875em;
    color: var(--clr-neutral-400);
    border-radius: var(--radius-400);
    transition: all 0.2s ease;
    cursor: pointer;
    font-weight: var(--fw-700);

    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
  }

  .primary {
    background: var(--clr-accent-400);
    color: var(--clr-neutral-100);
  }

  .primary:hover {
    background: var(--clr-accent-600);
  }
</style>

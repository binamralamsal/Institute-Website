<script lang="ts">
  import Button from "$lib/components/Button.svelte";
</script>

<aside class="course-sidebar">
  <Button size="large">
    Register
    <svg
      class="icon-tabler icon-tabler-arrow-right s-xcnQQNRdRv-M"
      fill="none"
      height="18"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
      stroke-width="2"
      viewBox="0 0 24 24"
      width="18"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M0 0h24v24H0z"
        fill="none"
        stroke="none"
        class="s-xcnQQNRdRv-M"
      />
      <line x1="5" x2="19" y1="12" y2="12" class="s-xcnQQNRdRv-M" /><line
        x1="13"
        x2="19"
        y1="18"
        y2="12"
        class="s-xcnQQNRdRv-M"
      />
      <line x1="13" x2="19" y1="6" y2="12" class="s-xcnQQNRdRv-M" />
    </svg>
  </Button>
</aside>

<style>
  .course-sidebar {
    background: white;
    border-radius: var(--radius-600);
    box-shadow: 0 10px 30px rgb(0 0 0 / 7%);
    align-self: flex-start;
    padding: 2.5rem;
    position: sticky;
    top: 5rem;
    display: flex;
    gap: 1rem;
    flex-direction: column;
  }

  @media screen and (max-width: 57em) {
    .course-sidebar {
      padding: 1rem 1.5rem 1rem 1.5rem;
    }
  }
</style>

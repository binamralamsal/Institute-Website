<script lang="ts">
  import Button from "$lib/components/Button.svelte";
  import Input from "$lib/components/Input.svelte";
</script>

<aside class="course-sidebar">
  <h2 class="form-title color-accent">Send Us A Message</h2>
  <Input placeholder="Eg. Alice Dsouza" label="Full Name" />
  <Input placeholder="Eg. +91 9876543210" label="Contact Number" />
  <Input placeholder="Eg. abc@email.com" label="Email Address" />
  <Input rows={3} label="Message" placeholder="Write something..." />

  <Button size="large">
    Send
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
  .form-title {
    margin: 0.5rem 0 0.6rem 0;
    font-size: var(--fs-500);
    font-weight: var(--fw-600);
  }
  .course-sidebar {
    background: white;
    border-radius: var(--radius-600);
    box-shadow: 0 10px 30px rgb(0 0 0 / 7%);
    align-self: flex-start;
    padding: 1.5rem;
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

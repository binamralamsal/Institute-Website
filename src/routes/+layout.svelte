<script lang="ts">
  import { Navbar } from "$lib/components";

  import "$lib/styles/css-reset.css";
  import "$lib/styles/styles.css";
  import "aos/dist/aos.css";

  import { onMount } from "svelte";
  import Aos from "aos";

  onMount(() => {
    Aos.init({ once: true, duration: 750 });
  });
</script>

<Navbar /><slot />

<script>
  import { onMount } from "svelte";
  import AboutSection from "./AboutSection.svelte";
  import BlogSection from "./BlogSection.svelte";
  import CoursesSection from "./CoursesSection.svelte";
  import EventsSection from "./EventsSection.svelte";
  import FeaturesSection from "./FeaturesSection.svelte";
  import HeroSection from "./HeroSection.svelte";
  import JobStagesSection from "./JobStagesSection.svelte";

  onMount(() => {
    // console.log;
  });

  // onMount(() => {
  // document.body.classList.add("transparent-nav");
  // });
</script>

<main>
  <HeroSection />
  <AboutSection />
  <JobStagesSection />
  <CoursesSection />
  <FeaturesSection />
  <EventsSection />
  <BlogSection />
</main>

<style>
</style>

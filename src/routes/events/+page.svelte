<script>
  import PageHeader from "$lib/components/PageHeader.svelte";
  import EventCard from "$lib/components/EventCard.svelte";
</script>

<svelte:head>
  <title>Events | KodiLearn - Committed to Learn Excellence in Education</title>
</svelte:head>

<PageHeader title="Events" />

<section class="container">
  <div class="events">
    <EventCard
      event={{
        date: new Date(),
        featuredImage: {
          alt: "Event",
          src: "/home/event-01.jpg",
        },
        location: "Alpaca Way Anaheim, CA 92805",
        title: "Innovation & Technological Entrepreneurship Team",
      }}
    />

    <EventCard
      event={{
        date: new Date(),
        featuredImage: {
          alt: "Event",
          src: "/home/event-02.jpg",
        },
        location: "Ritter Aveneue Detroit, MI 48226",
        title: "Virtual Spring Part-time Jobs Fair for Student",
      }}
    />

    <EventCard
      event={{
        date: new Date(),
        featuredImage: {
          alt: "Event",
          src: "/home/event-03.jpg",
        },
        location: "Stout Street Y ork, PA 17401",
        title: "Explorations of Regional Chief Executive Network",
      }}
    />
  </div>
</section>

<style>
  .container {
    padding: 8rem 0;
  }

  .events {
    display: flex;
    flex-direction: column;
    gap: 1.875rem;
    position: relative;
  }

  @media screen and (max-width: 50em) {
    .container {
      padding: 5rem 0;
    }
  }
</style>

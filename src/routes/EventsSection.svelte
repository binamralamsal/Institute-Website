<script>
  import EventCard from "$lib/components/EventCard.svelte";
</script>

<section class="events-section" aria-labelledby="events-title">
  <div class="container events-container">
    <header class="events-header">
      <h2 class="title" id="events-title">
        <span class="pre-title color-accent" data-aos="fade-up">
          Let's Learn Together
        </span>
        <span
          class="main-title color-heading"
          data-aos="fade-up"
          data-aos-delay="50"
        >
          Upcoming Educational Events
        </span>
      </h2>
    </header>

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
        data-aos="fade-up"
        data-aos-delay="100"
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
        data-aos="fade-up"
        data-aos-delay="200"
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
        data-aos="fade-up"
        data-aos-delay="300"
      />
    </div>
  </div>
</section>

<style>
  .events-section {
    padding: 8rem 0;
    overflow: hidden;
  }

  .events-container {
    text-align: center;
    position: relative;
  }

  .title > span {
    display: block;
  }

  .pre-title {
    font-weight: var(--fw-700);
    text-transform: uppercase;
    margin-bottom: 0.3125rem;
  }

  .main-title {
    font-size: var(--fs-700);
    font-weight: var(--fw-800);
    line-height: 1.4;
    margin-bottom: 3.5rem;
  }

  .events {
    display: flex;
    flex-direction: column;
    gap: 1.875rem;
  }

  @media screen and (max-width: 48em) {
    .events-section {
      padding: 5rem 0;
    }

    .main-title {
      margin-bottom: 2rem;
    }
  }
</style>

<script lang="ts">
  import Button from "./Button.svelte";

  export let event: {
    featuredImage: {
      alt: string;
      src: string;
    };
    title: string;
    date: Date;
    location: string;
  };
</script>

<div class="event" {...$$restProps}>
  <a href="/" class="event__image">
    <img
      src={event.featuredImage.src}
      alt={event.featuredImage.alt}
      height="140"
      width="140"
    /></a
  >

  <div class="event__description">
    <h3 class="event__title">
      <a href="/">{event.title}</a>
    </h3>

    <ul class="event__stats">
      <li class="event__stat">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="icon icon-tabler icon-tabler-calendar"
          width="18"
          height="18"
          viewBox="0 0 24 24"
          stroke-width="2"
          stroke="currentColor"
          fill="none"
          stroke-linecap="round"
          stroke-linejoin="round"
        >
          <path stroke="none" d="M0 0h24v24H0z" fill="none" />
          <path
            d="M4 5m0 2a2 2 0 0 1 2 -2h12a2 2 0 0 1 2 2v12a2 2 0 0 1 -2 2h-12a2 2 0 0 1 -2 -2zm12 -4l0 4m-8 -4l0 4m-4 4l16 0m-9 4l1 0l0 3"
          />
        </svg>
        {event.date.toLocaleDateString()}
      </li>
      <li class="event__stat">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="icon icon-tabler icon-tabler-clock"
          width="18"
          height="18"
          viewBox="0 0 24 24"
          stroke-width="2"
          stroke="currentColor"
          fill="none"
          stroke-linecap="round"
          stroke-linejoin="round"
        >
          <path stroke="none" d="M0 0h24v24H0z" fill="none" />
          <path d="M12 12m-9 0a9 9 0 1 0 18 0a9 9 0 1 0 -18 0m9 -5l0 5l3 3" />
        </svg>
        {event.date.toLocaleTimeString()}
      </li>
      <li class="event__stat">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="icon icon-tabler icon-tabler-map-pin"
          width="18"
          height="18"
          viewBox="0 0 24 24"
          stroke-width="2"
          stroke="currentColor"
          fill="none"
          stroke-linecap="round"
          stroke-linejoin="round"
        >
          <path stroke="none" d="M0 0h24v24H0z" fill="none" />
          <path
            d="M12 11m-3 0a3 3 0 1 0 6 0a3 3 0 1 0 -6 0m8.657 5.657l-4.243 4.243a2 2 0 0 1 -2.827 0l-4.244 -4.243a8 8 0 1 1 11.314 0z"
          />
        </svg>
        {event.location}
      </li>
    </ul>
  </div>

  <div class="event__btn">
    <Button size="large" href="#" variant="dark-primary">
      Book A Seat
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="icon icon-tabler icon-tabler-arrow-right"
        width="18"
        height="18"
        viewBox="0 0 24 24"
        stroke-width="2"
        stroke="currentColor"
        fill="none"
        stroke-linecap="round"
        stroke-linejoin="round"
      >
        <path stroke="none" d="M0 0h24v24H0z" fill="none" />
        <line x1="5" y1="12" x2="19" y2="12" />
        <line x1="13" y1="18" x2="19" y2="12" />
        <line x1="13" y1="6" x2="19" y2="12" />
      </svg>
    </Button>
  </div>
</div>

<style>
  .event {
    border: 1px solid #eee;
    display: grid;
    grid-template-columns: 2fr 7fr 2fr;
    align-items: center;
    text-align: left;
    padding: 1.25rem;

    transition: 0.4s;
    border-radius: var(--radius-400);
  }

  .event:hover {
    box-shadow: 0 10px 30px rgb(0 0 0 / 7%);
  }

  .event img {
    object-fit: cover;
    height: 100%;
    aspect-ratio: 1/1;
  }

  .event__title {
    font-size: 1.5rem;
    margin-bottom: 1rem;
    font-weight: var(--fw-700);
    color: var(--clr-heading);
  }

  .event__stats {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    gap: 2rem;
  }

  .event__stat {
    align-items: center;
    display: flex;
    gap: 0.5rem;
  }

  ul {
    list-style-type: none;
  }

  .event__btn {
    display: flex;
    justify-content: flex-end;
  }

  @media screen and (max-width: 69em) {
    .event__image {
      grid-row: span 2;
    }

    .event {
      gap: 1.25rem;
      align-items: flex-start;
      grid-template-columns: 2fr 8fr;
    }

    .event__btn {
      grid-row-start: 2;
      grid-column-start: 2;
      justify-self: flex-start;
    }
  }

  @media screen and (max-width: 48em) {
    .event {
      grid-template-columns: 1fr;
    }

    .event__image {
      grid-row-start: 1;
    }

    .event img {
      width: 100%;
    }

    .event__description {
      grid-row-start: 2;
    }

    .event__stats {
      gap: 1rem;
    }

    .event__btn {
      grid-row-start: 3;
      grid-column-start: 1;
    }
  }
</style>

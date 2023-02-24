<script lang="ts">
  import PageHeader from "$lib/components/PageHeader.svelte";
  import Button from "$lib/components/Button.svelte";
</script>

<svelte:head>
  <title>Contact | KodiLearn - Committed to Learn Excellence in Education</title
  >
</svelte:head>

<PageHeader title="Contact" />

<section aria-labelledby="contact-title" class="contact-section">
  <div class="container contact-container">
    <header class="contact-header">
      <h2 class="title" id="contact-title">
        <span class="pre-title color-accent"> Need Help? </span>
        <span class="main-title color-heading"> Get In Touch With us </span>
      </h2>
    </header>

    <div class="even-columns contact-grid">
      <div class="cards even-columns">
        <div class="card card-01">
          <div class="icon">
            <svg
              class=" icon-tabler icon-tabler-world-www"
              fill="none"
              height="25"
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              viewBox="0 0 24 24"
              width="25"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path d="M0 0h24v24H0z" fill="none" stroke="none" />
              <path d="M19.5 7a9 9 0 0 0 -7.5 -4a8.991 8.991 0 0 0 -7.484 4" />
              <path d="M11.5 3a16.989 16.989 0 0 0 -1.826 4" />
              <path d="M12.5 3a16.989 16.989 0 0 1 1.828 4" />
              <path d="M19.5 17a9 9 0 0 1 -7.5 4a8.991 8.991 0 0 1 -7.484 -4" />
              <path d="M11.5 21a16.989 16.989 0 0 1 -1.826 -4" />
              <path d="M12.5 21a16.989 16.989 0 0 0 1.828 -4" />
              <path d="M2 10l1 4l1.5 -4l1.5 4l1 -4" />
              <path d="M17 10l1 4l1.5 -4l1.5 4l1 -4" />
              <path d="M9.5 10l1 4l1.5 -4l1.5 4l1 -4" />
            </svg>
          </div>

          <h3 class="title">Our Website</h3>

          <div class="card-details">
            <a href="#" target="_blank">www.eduvibe.com</a>
            <a href="#" target="_blank">www.wpvibe.com</a>
          </div>
        </div>

        <div class="card card-02">
          <div class="icon">
            <svg
              class=" icon-tabler icon-tabler-phone"
              fill="none"
              height="25"
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              viewBox="0 0 24 24"
              width="25"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path d="M0 0h24v24H0z" fill="none" stroke="none" />
              <path
                d="M5 4h4l2 5l-2.5 1.5a11 11 0 0 0 5 5l1.5 -2.5l5 2v4a2 2 0 0 1 -2 2a16 16 0 0 1 -15 -15a2 2 0 0 1 2 -2"
              />
            </svg>
          </div>

          <h3 class="title">Call Us</h3>

          <div class="card-details">
            <p>+91 9172124795</p>
            <p>+91 8459231328</p>
          </div>
        </div>

        <div class="card card-03">
          <div class="icon">
            <svg
              class=" icon-tabler icon-tabler-mail"
              fill="none"
              height="25"
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              viewBox="0 0 24 24"
              width="25"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path d="M0 0h24v24H0z" fill="none" stroke="none" />
              <path
                d="M3 5m0 2a2 2 0 0 1 2 -2h14a2 2 0 0 1 2 2v10a2 2 0 0 1 -2 2h-14a2 2 0 0 1 -2 -2z"
              />
              <path d="M3 7l9 6l9 -6" />
            </svg>
          </div>

          <h3 class="title">Email Us</h3>

          <div class="card-details">
            <a href="#" target="_blank">eduvibe@mail.com</a>
            <a href="#" target="_blank">wpvibe@mail.com</a>
          </div>
        </div>

        <div class="card card-04">
          <div class="icon">
            <svg
              class=" icon-tabler icon-tabler-map-pin-filled"
              fill="none"
              height="25"
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              viewBox="0 0 24 24"
              width="25"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path d="M0 0h24v24H0z" fill="none" stroke="none" />
              <path
                d="M18.364 4.636a9 9 0 0 1 .203 12.519l-.203 .21l-4.243 4.242a3 3 0 0 1 -4.097 .135l-.144 -.135l-4.244 -4.243a9 9 0 0 1 12.728 -12.728zm-6.364 3.364a3 3 0 1 0 0 6a3 3 0 0 0 0 -6z"
                fill="currentColor"
                stroke-width="0"
              />
            </svg>
          </div>

          <h3 class="title">Our Location</h3>

          <div class="card-details">
            <p>486 Normana Avenue Morningtide, 4223</p>
          </div>
        </div>
      </div>
      <div class="form">
        <input placeholder="Name*" type="text" />
        <input placeholder="Email*" type="email" />
        <input placeholder="Phone" type="text" />
        <input placeholder="Subject*" type="text" />
        <textarea placeholder="Your Message*" rows="6" />

        <Button href="/about">
          <span> Learn More </span>
          <svg
            class="icon-tabler icon-tabler-arrow-right"
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
            <path d="M0 0h24v24H0z" fill="none" stroke="none" />
            <line x1="5" x2="19" y1="12" y2="12" />
            <line x1="13" x2="19" y1="18" y2="12" />
            <line x1="13" x2="19" y1="6" y2="12" />
          </svg>
        </Button>
      </div>
    </div>

    <div class="map">
      <iframe
        aria-hidden="false"
        src="https://maps.google.com/maps?q=2880%20Broadway,%20New%20York&amp;t=&amp;z=13&amp;ie=UTF8&amp;iwloc=&amp;output=embed"
        tabindex="0"
        title="Google Map"
      />
    </div>
  </div>
</section>

<style>
  .contact-section {
    padding: 8rem 0;
    overflow: hidden;
  }

  .contact-container {
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
    margin-bottom: 2.5rem;
  }

  .contact-grid {
    gap: 6.25rem;
  }

  .cards {
    gap: 1.875rem;
  }

  .card {
    padding: 3.125rem 1.25rem;
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.06);
    border-radius: var(--radius-500);
  }

  .icon {
    display: inline-flex;
    padding: 0.9rem;
    border-radius: 100%;
  }

  .title {
    margin: 1.25rem 0 0.9375rem 0;
    font-weight: var(--fw-800);
  }

  .card-01 .icon,
  .card-04 .icon {
    background: hsla(219, 87%, 51%, 0.1);
    color: var(--clr-accent-400);
  }

  .card-02 .icon,
  .card-03 .icon {
    background: rgba(251, 124, 86, 0.1);
    color: var(--clr-secondary-400);
  }

  .card-03 .icon {
    background: rgba(255, 164, 27, 0.1);
  }

  .card:hover {
    background: var(--clr-secondary-400);
    color: white;
    transition: 0.4s;
    transform: translateY(-15px);
  }

  .card:hover a {
    color: white;
    transition: 0.4s;
  }

  .card:hover .icon {
    background: white;
    color: var(--clr-secondary-400);
    transition: 0.4s;
  }

  .form {
    display: flex;
    flex-direction: column;
    gap: 1.25rem;
  }

  input,
  textarea {
    background: #f5f5f5;
    border: 1px solid transparent;
    border-radius: var(--radius-500);
    outline: transparent;
    padding: 1rem 1.875rem;
    transition: 0.4s;
  }

  input:focus,
  textarea:focus {
    border-color: var(--clr-accent-400);
  }

  textarea {
    resize: vertical;
  }

  iframe {
    height: 31.25rem;
    border: 0;
    width: 100%;
    margin-top: 5rem;
  }

  @media screen and (max-width: 62.5em) {
    .contact-grid {
      gap: 3rem;
    }

    .cards {
      grid-template-columns: 1fr;
    }
  }

  @media screen and (max-width: 48em) {
    .contact-section {
      padding: 5rem 0;
    }

    .cards {
      grid-template-columns: 1fr 1fr;
    }
  }

  @media screen and (max-width: 32em) {
    .cards {
      grid-template-columns: 1fr;
    }
  }
</style>

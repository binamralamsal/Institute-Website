<section class="hero-section" aria-labelledby="hero-title">
  <div class="container hero-container even-columns">
    <div>
      <header>
        <span class="pre-title color-accent" data-aos="fade-up"
          >Better learning future with us</span
        >
        <h1
          class="title"
          id="hero-title"
          data-aos="fade-up"
          data-aos-delay="150"
        >
          Committed To Learn Excellence In Education
        </h1>
      </header>
      <p class="caption" data-aos="fade-up" data-aos-delay="300">
        It is long established that a reader will be distracted by the readable
        popular and best content.
      </p>
    </div>
    <div class="right-images">
      <img
        class="girl-image"
        src="/home/girl-thumb.png"
        alt="Girl thumbchecking"
        data-aos="fade-left"
        height="780"
        data-aos-delay="450"
      />
      <img
        class="girl-bg"
        src="/home/girl-bg.png"
        data-aos="fade-left"
        alt="Girl background"
        data-aos-delay="600"
      />
    </div>
  </div>

  <div class="decorations">
    <img src="/home/shape-1.png" alt="Decoration 1" class="shape-1" />
    <img src="/home/shape-3.png" alt="Decoration 3" class="shape-3" />
  </div>
</section>

<style>
  .hero-section {
    background: url("/home/hero-background.jpg");
    background-repeat: no-repeat;
    background-size: cover;
  }

  .hero-container {
    padding: 12rem 0 10rem 0;
    position: relative;
  }

  .pre-title {
    font-weight: var(--fw-700);
    display: flex;
    align-items: center;
    gap: 0.5em;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin-bottom: 0.625rem;
  }

  .pre-title::before {
    content: "";
    height: 0.15em;
    background: var(--clr-accent-400);
    width: 3.125em;
  }

  .title {
    font-size: var(--fs-900);
    font-weight: var(--fw-800);
    color: var(--clr-accent-900);
    margin-bottom: 1.875rem;
    line-height: 1.25;
    max-width: 13ch;
  }

  .caption {
    font-size: var(--fs-500);
    line-height: 2em;
    max-width: 45ch;
  }

  .girl-bg,
  .girl-image {
    position: absolute;
    right: 0;
    bottom: 0;
    height: 85%;
  }

  .girl-bg {
    height: 75%;
  }

  .right-images::before {
    content: url("/home/shape-2.png");
    position: relative;
    top: 0;
    left: 0;
  }

  .shape-1,
  .shape-3 {
    position: absolute;
  }

  .shape-1 {
    left: 10px;
    top: 90px;
  }

  .shape-3 {
    top: 250px;
    right: 5%;
  }

  @media screen and (max-width: 68em) {
    .shape-1 {
      display: none;
    }

    .girl-image {
      height: 60%;
    }

    .girl-bg {
      height: 50%;
    }
  }

  @media screen and (max-width: 56.25em) {
    .hero-container {
      grid-template-columns: 1fr;
      padding: 8rem 0 6rem 0;
    }

    .title,
    .caption {
      max-width: 100%;
    }

    .girl-image,
    .girl-bg,
    .shape-1,
    .shape-3,
    .right-images::before {
      display: none;
    }
  }
</style>

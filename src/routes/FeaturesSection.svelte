<script>
  import Button from "$lib/components/Button.svelte";
</script>

<section class="features-section" aria-labelledby="features-title">
  <div class="container features-container even-columns">
    <div class="image" data-aos="fade-right">
      <img src="/home/features-image.jpg" alt="Features" />
    </div>
    <div class="description">
      <header data-aos="fade-left">
        <span class="pre-title color-accent">Who we are</span>
        <h2 class="title" id="features-title">We Offer The Best Carrier</h2>
      </header>

      <div class="services">
        <div class="service" data-aos="fade-up" data-aos-delay="100">
          <div class="service__icon">asdf</div>
          <div class="service__content">
            <h3 class="service__title">Earn Money with Unique Projects</h3>
            <p>
              If a student creates a unique project, we assist them so that they
              can earn money.
            </p>
          </div>
        </div>

        <div class="service" data-aos="fade-up" data-aos-delay="200">
          <div class="service__icon">asdf</div>
          <div class="service__content">
            <h3 class="service__title">Freelancing for profit</h3>
            <p>
              Learn how to work as a freelancer and make money through our
              instructors.
            </p>
          </div>
        </div>

        <div class="service" data-aos="fade-up" data-aos-delay="300">
          <div class="service__icon">asdf</div>
          <div class="service__content">
            <h3 class="service__title">Experience and learn at Journey</h3>
            <p>
              Participate in paid or unpaid internships and receive a
              certificate upon completion.
            </p>
          </div>
        </div>

        <div class="service" data-aos="fade-up" data-aos-delay="400">
          <div class="service__icon">asdf</div>
          <div class="service__content">
            <h3 class="service__title">Boost your learning with resources</h3>
            <p>
              Access resources, materials, and quizzes on our Telegram channel
              to enhance your knowledge.
            </p>
          </div>
        </div>
      </div>

      <div class="features-btn" data-aos="fade-up" data-aos-delay="500">
        <Button href="#">
          <span>Know About Us</span>
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
  </div>
</section>

<style>
  .features-section {
    padding: 8rem 0;
    overflow: hidden;
    background: url("/home/features-bg.jpg");
    background-size: cover;
  }

  .features-container {
    gap: 3rem;
    align-items: center;
    position: relative;
  }

  .features-container::before,
  .features-container::after {
    position: absolute;
    right: -20%;
  }

  .features-container::before {
    content: url("/home/features-decoration-1.png");
    top: 10%;
  }

  .features-container::after {
    content: url("/home/features-decoration-2.png");
    bottom: 10%;
  }

  .image {
    position: relative;
  }

  .image img {
    z-index: 20;
    position: relative;
  }

  .image::before,
  .image::after {
    position: absolute;
  }

  .image::before {
    content: url("/home/features-image-1.jpg");
    top: 10%;
    left: -15%;
    z-index: 10;
  }

  .image::after {
    content: url("/home/features-image-2.jpg");
    bottom: 10%;
    right: 0%;
    z-index: 30;
  }

  .pre-title {
    font-weight: var(--fw-700);
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin-bottom: 0.625rem;
    display: block;
  }

  .title {
    font-size: var(--fs-700);
    font-weight: var(--fw-800);
    color: var(--clr-heading);
    line-height: 1.4;
  }

  .services {
    margin-top: 2.5rem;
  }

  .services {
    display: flex;
    flex-direction: column;
    gap: 1.875rem;
  }

  .service {
    display: flex;
    gap: 1.5625rem;
  }

  .service__icon {
    align-self: flex-start;
    border-radius: 100%;
  }

  .service__title {
    color: var(--clr-accent-900);
    margin-bottom: 0.3125rem;
    font-size: 1.25rem;
    font-weight: var(--fw-700);
  }

  .features-btn {
    margin-top: 3.75rem;
  }

  @media screen and (max-width: 75em) {
    .image::before {
      display: none;
    }
  }

  @media screen and (max-width: 60em) {
    .image::after {
      display: none;
    }
  }

  @media screen and (max-width: 48em) {
    .image img {
      width: 100%;
    }

    .features-container::before,
    .features-container::after {
      display: none;
    }
  }

  @media screen and (max-width: 40em) {
    .features-section {
      padding: 5rem 0;
    }

    .image::before,
    .image::after {
      display: none;
    }
  }
</style>

<script lang="ts">
  let navbarOpened = false;
  let scrolled = false;

  const handleOnScroll = () => {
    if (window.scrollY > 100) {
      return (scrolled = true);
    }

    return (scrolled = false);
  };
</script>

<svelte:window on:scroll={handleOnScroll} />

<header class="navbar-wrapper transparent" class:scrolled>
  <div class="container nav-container">
    <a href="/" data-aos="fade-right">Kodilearn</a>

    <button
      class="mobile-nav-toggle"
      class:active={navbarOpened}
      aria-controls="primary-navigation"
      aria-expanded={navbarOpened}
      aria-label="toggle navigation"
      on:click={() => (navbarOpened = !navbarOpened)}
    >
      <span />
      <span />
      <span />
    </button>

    <nav
      id="primary-navigation"
      class="primary-navigation"
      class:active={navbarOpened}
      data-aos="fade-left"
      data-aos-delay="250"
    >
      <ul class="nav-links">
        <li>
          <a href="/" class="nav-link active">Home</a>
        </li>
        <li>
          <a href="/courses" class="nav-link">Courses</a>
        </li>
        <li>
          <a href="/events" class="nav-link">Events</a>
        </li>
        <li>
          <a href="/blogs" class="nav-link">Blogs</a>
        </li>
        <li>
          <a href="/contact" class="nav-link">Contact</a>
        </li>
        <li>
          <a href="/about" class="nav-link">About</a>
        </li>
      </ul>
    </nav>
  </div>
</header>

<style>
  .navbar-wrapper {
    padding: 1rem 0;
    position: relative;
    top: 0;
    z-index: 999;
  }

  .navbar-wrapper.transparent {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
  }

  .navbar-wrapper.scrolled {
    padding: 0.5rem 0;
    position: sticky;
    background-color: white;
    animation: headerSticky 0.95s ease forwards;
  }

  .navbar-wrapper.transparent.scrolled {
    position: fixed;
  }

  @keyframes headerSticky {
    from {
      transform: translateY(-100%);
    }
    to {
      transform: translateY(0);
    }
  }

  .nav-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .nav-links {
    list-style-type: none;
    display: flex;
    gap: 0.5rem;
  }

  .nav-link {
    padding: 1rem;
    text-decoration: none;
    display: inline-block;
    transition: color 0.2s ease;
    color: var(--clr-neutral-400);
    font-weight: var(--fw-600);
  }

  .nav-link.active {
    color: var(--clr-accent-400);
  }

  .nav-link:hover {
    color: var(--clr-accent-600);
  }

  .mobile-nav-toggle {
    display: none;
    background: none;
    border: 0;
    flex-direction: column;
    padding: 0.5rem;
    cursor: pointer;
    gap: 0.3rem;
  }

  .mobile-nav-toggle span {
    background: var(--clr-neutral-400);
    display: inline-block;
    padding: 0.05rem 0.55rem;
    transition: all 0.2s ease 0s;
    transform-origin: left center;
  }

  .mobile-nav-toggle.active span:first-child {
    transform: rotate(45deg);
  }

  .mobile-nav-toggle.active span:nth-child(2) {
    opacity: 0;
  }

  .mobile-nav-toggle.active span:last-child {
    transform: rotate(-45deg);
  }

  @media screen and (max-width: 40em) {
    .navbar-wrapper {
      padding: 0.5rem 0;
    }

    .primary-navigation {
      display: none;
      position: absolute;
      top: 100%;
      height: 0;
      background: white;
      left: 0;
      animation: height 0.2s ease;
      right: 0;
    }

    .primary-navigation.active {
      display: block;
      height: auto;
    }

    .nav-links {
      flex-direction: column;
      gap: 0;
    }

    .mobile-nav-toggle {
      display: flex;
    }

    .nav-link {
      width: 100%;
      padding: 0.5rem 2rem;
    }
  }
</style>

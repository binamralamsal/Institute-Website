<script>
  import BlogCard from "$lib/components/BlogCard.svelte";
</script>

<section class="blog-section" aria-labelledby="blog-title">
  <div class="container blog-container">
    <header class="blog-header">
      <h2 class="title" id="blog-title">
        <span class="pre-title color-accent" data-aos="fade-up">
          Latest From News
        </span>
        <span
          class="main-title color-heading"
          data-aos="fade-up"
          data-aos-delay="50"
        >
          Get Our Every News & Blog</span
        >
      </h2>
    </header>

    <div class="blog-cards even-columns">
      <BlogCard
        blog={{
          category: "Business",
          date: new Date(),
          image: {
            alt: "Post 1",
            src: "/home/post-01.jpg",
          },
          title: "Introduction to Javascript for the Beginners",
        }}
        data-aos="fade-up"
        data-aos-delay="100"
      />
      <BlogCard
        blog={{
          category: "Education",
          date: new Date(),
          image: {
            alt: "Post 2",
            src: "/home/post-02.jpg",
          },
          title: "Identify Design for a New Courses Crusader Work",
        }}
        data-aos="fade-up"
        data-aos-delay="200"
      />
      <BlogCard
        blog={{
          category: "Web Development",
          date: new Date(),
          image: {
            alt: "Post 3",
            src: "/home/post-03.jpg",
          },
          title: "Grow Your Students Base With Free Courses",
        }}
        data-aos="fade-up"
        data-aos-delay="300"
      />
    </div>
  </div>
</section>

<style>
  .blog-section {
    padding: 8rem 0;
    overflow: hidden;
    background: url("/home/blog-bg.jpg");
    background-size: cover;
  }

  .blog-container {
    text-align: center;
    position: relative;
  }

  .blog-container::before,
  .blog-container::after,
  .blog-cards::before,
  .blog-cards::after {
    position: absolute;
  }

  .blog-container::before {
    content: url("/home/blog-decoration-1.png");
    left: -23%;
    transform: scale(0.6);
    top: -15%;
  }

  .blog-container::after {
    content: url("/home/blog-decoration-2.png");
    right: -15%;
    top: -15%;
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

  .blog-cards {
    text-align: initial;
    grid-template-columns: 1fr 1fr 1fr;
    align-items: flex-start;
    gap: 1.875rem;
    position: relative;
  }

  .blog-cards::before {
    content: url("/home/blog-decoration-3.png");
    bottom: -15%;
    left: -5%;
  }

  .blog-cards::after {
    content: url("/home/blog-decoration-4.png");
    bottom: -20%;
    right: -15%;
  }

  @media screen and (max-width: 59em) {
    .blog-container::before,
    .blog-container::after,
    .blog-cards::before,
    .blog-cards::after {
      display: none;
    }

    .blog-cards {
      grid-template-columns: 1fr 1fr;
    }
  }

  @media screen and (max-width: 48em) {
    .blog-section {
      padding: 5rem 0;
    }

    .blog-cards {
      grid-template-columns: 1fr;
    }
  }
</style>

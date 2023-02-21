<script>
  import BlogCard from "$lib/components/BlogCard.svelte";
</script>

<section aria-labelledby="related-blogs-title" class="related-blogs-section">
  <div class="container related-blogs-container">
    <header data-aos="fade-right">
      <span class="pre-title color-accent">Related Blogs</span>
      <h2 class="title color-heading" id="related-blogs-title">
        Blogs You May Like
      </h2>
    </header>

    <div class="even-columns blogs-cards">
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
  .related-blogs-section {
    margin-top: 4rem;
    overflow: hidden;
  }

  .related-blogs-container {
    gap: 3rem;
    align-items: center;
    position: relative;
  }

  .pre-title {
    font-weight: var(--fw-700);
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin-bottom: 0.625rem;
    display: block;
  }

  .title {
    font-size: var(--fs-600);
    font-weight: var(--fw-800);
    line-height: 1.4;
    margin-bottom: 2.5rem;
  }

  .blogs-cards {
    text-align: initial;
    grid-template-columns: 1fr 1fr;
    align-items: flex-start;
    gap: 1.875rem;
  }

  @media screen and (max-width: 46em) {
    .blogs-cards {
      grid-template-columns: 1fr;
    }
  }
</style>

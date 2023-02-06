<script>
  import CourseCard from "$lib/components/CourseCard.svelte";
</script>

<section
  class="related-courses-section"
  aria-labelledby="related-courses-title"
>
  <div class="container related-courses-container">
    <header data-aos="fade-right">
      <span class="pre-title color-accent">Related Courses</span>
      <h2 class="title color-heading" id="related-courses-title">
        Courses You May Like
      </h2>
    </header>

    <div class="even-columns courses-cards">
      <CourseCard
        course={{
          duration: "2 weeks",
          image: {
            alt: "Course",
            src: "/courses/course-01.jpg",
          },
          numberOfModules: 20,
          title: "Complete Typescript course",
        }}
        data-aos="fade-up"
        data-aos-delay="100"
      />
      <CourseCard
        course={{
          duration: "2 weeks",
          image: {
            alt: "Course",
            src: "/courses/course-02.jpg",
          },
          numberOfModules: 20,
          title: "Complete Bun.js course",
        }}
        data-aos="fade-up"
        data-aos-delay="200"
      />
      <CourseCard
        course={{
          duration: "2 weeks",
          image: {
            alt: "Course",
            src: "/courses/course-03.jpg",
          },
          numberOfModules: 20,
          title: "Complete CSS3 course",
        }}
        data-aos="fade-up"
        data-aos-delay="300"
      />
    </div>
  </div>
</section>

<style>
  .related-courses-section {
    padding: 0 0 8rem 0;
    overflow: hidden;
  }

  .related-courses-container {
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
    font-size: var(--fs-700);
    font-weight: var(--fw-800);
    line-height: 1.4;
    margin-bottom: 2.5rem;
  }

  .courses-cards {
    text-align: initial;
    grid-template-columns: 1fr 1fr 1fr;
    align-items: flex-start;
    gap: 1.875rem;
  }

  @media screen and (max-width: 57em) {
    .courses-cards {
      grid-template-columns: 1fr 1fr;
    }
  }

  @media screen and (max-width: 40em) {
    .courses-cards {
      grid-template-columns: 1fr;
    }
  }
</style>

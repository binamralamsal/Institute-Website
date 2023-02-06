<script>
  import CourseCard from "$lib/components/CourseCard.svelte";
  import PageHeader from "$lib/components/PageHeader.svelte";
</script>

<svelte:head>
  <title>
    Courses | KodiLearn - Committed to Learn Excellence in Education
  </title>
</svelte:head>

<PageHeader title="Courses" />

<section class="container courses">
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

    <CourseCard
      course={{
        duration: "2 weeks",
        image: {
          alt: "Course",
          src: "/courses/course-04.jpg",
        },
        numberOfModules: 20,
        title: "Machine Learning A-Z: Hands-On Python and java",
      }}
      data-aos="fade-up"
      data-aos-delay="400"
    />
    <CourseCard
      course={{
        duration: "2 weeks",
        image: {
          alt: "Course",
          src: "/courses/course-05.jpg",
        },
        numberOfModules: 20,
        title: "Data Structure and Algorithms",
      }}
      data-aos="fade-up"
      data-aos-delay="500"
    />
    <CourseCard
      course={{
        duration: "2 weeks",
        image: {
          alt: "Course",
          src: "/courses/course-06.jpg",
        },
        numberOfModules: 20,
        title: "Rust crash course for beginners",
      }}
      data-aos="fade-up"
      data-aos-delay="600"
    />
  </div>
</section>

<style>
  .courses {
    padding: 8rem 0;
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

  @media screen and (max-width: 48em) {
    .courses {
      padding: 5rem 0;
    }
  }

  @media screen and (max-width: 40em) {
    .courses-cards {
      grid-template-columns: 1fr;
    }
  }
</style>

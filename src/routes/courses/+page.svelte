<script>
  import CourseCard from "$lib/components/CourseCard.svelte";
</script>

<section class="course-header">
  <div class="container">
    <h1 class="page-title color-heading">Courses</h1>
    <nav class="breadcrumb">
      <ul>
        <li>
          <a href="/">Home</a>
        </li>
        <li class="separator">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="icon icon-tabler icon-tabler-chevron-right"
            width="16"
            height="16"
            viewBox="0 0 24 24"
            stroke-width="2"
            stroke="currentColor"
            fill="none"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <path stroke="none" d="M0 0h24v24H0z" fill="none" />
            <path d="M9 6l6 6l-6 6" />
          </svg>
        </li>
        <li>Courses</li>
      </ul>
    </nav>
  </div>
</section>

<section class="container courses">
  <div class="even-columns courses-cards">
    <CourseCard
      course={{
        duration: "2 weeks",
        image: {
          alt: "Course",
          src: "/home/course-01.jpg",
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
          src: "/home/course-02.jpg",
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
          src: "/home/course-03.jpg",
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
          src: "/home/course-04.jpg",
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
          src: "/home/course-05.jpg",
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
          src: "/home/course-06.jpg",
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
  .course-header {
    padding: 3.75rem 0;
    background: url("/home/header-bg.jpg");
  }

  .page-title {
    margin-bottom: 0.3125rem;
    font-size: var(--fs-700);
    font-weight: var(--fw-800);
    line-height: 1.4;
  }

  ul {
    list-style-type: none;
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }

  ul,
  a {
    color: var(--clr-neutral-400);
  }

  a:hover {
    color: var(--clr-accent-400);
  }

  ul li {
    display: flex;
  }

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

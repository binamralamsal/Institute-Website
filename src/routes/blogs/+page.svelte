<script>
  import PageHeader from "$lib/components/PageHeader.svelte";
  import BlogCard from "$lib/components/BlogCard.svelte";
</script>

<svelte:head>
  <title>Blog | KodiLearn - Committed to Learn Excellence in Education</title>
</svelte:head>

<PageHeader title="Blogs" />

<section class="container blogs">
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
</section>

<style>
  .blogs {
    padding: 8rem 0;
  }

  .blog-cards {
    text-align: initial;
    grid-template-columns: 1fr 1fr 1fr;
    align-items: flex-start;
    gap: 1.875rem;
    position: relative;
  }

  @media screen and (max-width: 59em) {
    .blog-cards {
      grid-template-columns: 1fr 1fr;
    }
  }

  @media screen and (max-width: 48em) {
    .blog-cards {
      grid-template-columns: 1fr;
    }
  }

  @media screen and (max-width: 48em) {
    .blogs {
      padding: 5rem 0;
    }
  }

  @media screen and (max-width: 40em) {
  }
</style>

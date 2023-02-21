<script lang="ts">
  import PageHeader from "$lib/components/PageHeader.svelte";
  import RelatedBlogs from "./RelatedBlogs.svelte";
</script>

<svelte:head>
  <title>Introduction to TypeScript | KodiLearn</title>
</svelte:head>

<PageHeader
  breadcrumbs={[{ href: "/blogs", title: "Blogs" }]}
  title="Introduction to TypeScript"
/>

<div class="container article-container">
  <section class="stats">
    <a class="category" href="#">Web Development</a>

    <div class="blog-meta">
      <div class="date">
        <svg
          class="icon icon-tabler icon-tabler-calendar"
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
          <path
            d="M4 5m0 2a2 2 0 0 1 2 -2h12a2 2 0 0 1 2 2v12a2 2 0 0 1 -2 2h-12a2 2 0 0 1 -2 -2z"
          />
          <path d="M16 3l0 4" />
          <path d="M8 3l0 4" />
          <path d="M4 11l16 0" />
          <path d="M11 15l1 0" />
          <path d="M12 15l0 3" />
        </svg>
        <time datetime="2020-01-01">January 1, 2020</time>
      </div>
      <div class="time-read">
        <svg
          class="icon icon-tabler icon-tabler-clock"
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
          <path d="M12 12m-9 0a9 9 0 1 0 18 0a9 9 0 1 0 -18 0" />
          <path d="M12 7l0 5l3 3" />
        </svg>6 min read
      </div>
    </div>
  </section>

  <article class="blog-content">
    <strong class="title">Introduction to TypeScript</strong>

    <div class="img-wrapper">
      <img
        alt="Course Image"
        class="thumbnail"
        src="/courses/course-thumbnail.jpg"
      />
    </div>

    <p>
      Grursus mal suada faci lisis Lorem ipsum dolarorit more ametion
      consectetur elit. Vesti at bulum nec the odio aea the dumm ipsumm ipsum
      that dolocons rsus mal suada and fadolorit to the consectetur elit. All
      the Lorem Ipsum generators on the Internet tend to repeat that predefined
      chunks as necessary making this the first true dummy generator on the
      Internet.Grursus mal suada faci lisis Lorem ipsum dolarorit more ametion
      consectetur elit. Vesti at bulum nec odio aea the dumm ipsumm ipsum that
      dolocons rsus mal suada and fadolorit to the consectetur elit.
    </p>
    <p>
      Grursus mal suada faci lisis Lorem ipsum dolarorit more ametion
      consectetur elit. Vesti at bulum nec at odio aea the dumm ipsumm ipsum
      that dolocons rsus mal suada and fadolorit to the consectetur elit. All
      the Lorem Ipsum generators on the Internet tend.
    </p>

    <blockquote>
      "This is a Quote quis eleifend quam adipiscing vitae aliquet bibendum enim
      facilisis gravida neque velit euismod in pellentesque massa placerat
      volutpat lacus laoreet non curabitured gravida odio aenean sed
      adipiscing."
    </blockquote>

    <h2>The 3 most important things to consider</h2>
    <p>
      Grursus mal suada faci lisis Lorem ipsum dolarorit more ametion
      consectetur elit. Vesti at bulum nec odio aea the dumm ipsumm ipsum that
      dolocons rsus mal suada and fadolorit to the consectetur dummy read more
      elit.Grursus mal suada faci lisis Lorem ipsum dolarorit more ametion
      consectetur elit. Vesti at bulum nec that dolocons rsus mal suada and
      fadolorit to the consectetur elit.
    </p>
    <ul>
      <li>
        Struggling to sell one multi-million dollar home currently on the market
      </li>
      <li>
        The point of using Lorem Ipsum is that it has a normal distribution of
        letters.
      </li>
      <li>
        Publishing packages and web page editors now use their default model
        text.
      </li>
      <li>
        Publishing packages and web page editors now use their default model
        text.
      </li>
    </ul>

    <div class="img-gallery">
      <img alt="Course" src="/courses/course-01.jpg" />
      <img alt="Course" src="/courses/course-02.jpg" />
    </div>

    <h2>Learned From Doing One Of Those Social Media</h2>

    <p>
      Grursus mal suada faci lisis Lorem ipsum dolarorit more ametion
      consectetur elit. Vesti at bulum nec the odio aea the dumm ipsumm ipsum
      that dolocons rsus mal suada and fadolorit to the consectetur elit. All
      the Lorem Ipsum generators on the Internet tend to repeat that predefined
      chunks as necessary making this the first true dummy generator on the
      Internet.Grursus mal suada faci lisis Lorem ipsum dolarorit more ametion
      consectetur elit.
    </p>
  </article>

  <section class="bottom-stats">
    <ul class="tags">
      <li>e-Learning</li>
      <li>Online Courses</li>
      <li>Finance</li>
    </ul>

    <div class="share">
      <p>Share:</p>
    </div>
  </section>

  <RelatedBlogs />
</div>

<style>
  .article-container {
    max-width: 60rem;
    margin-top: 10rem;
    margin-bottom: 8rem;
  }

  .stats,
  .blog-meta {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }

  .category {
    text-transform: uppercase;
    font-weight: var(--fw-600);
  }

  .stats {
    justify-content: space-between;
  }

  .blog-meta {
    gap: 3.125rem;
  }

  .blog-meta div {
    gap: 0.5rem;
    display: flex;
    align-items: center;
  }

  .blog-content {
    display: flex;
    flex-direction: column;
    gap: 1.875rem;
    margin: 1.875rem 0;
    line-height: 1.625;
  }

  .title {
    font-size: var(--fs-600);
    font-weight: var(--fw-800);
    display: inline-block;
  }

  .img-wrapper {
    margin: 0 -6.5625rem;
  }

  .thumbnail {
    border-radius: var(--radius-600);
    width: 100%;
  }

  .blog-content blockquote {
    padding: 1.5625rem;
    font-size: var(--fs-500);
    font-weight: var(--fw-500);
    border-radius: var(--radius-500);
    border-top: 3px solid var(--clr-accent-400);
    text-align: center;
    box-shadow: 0 8px 25px rgba(0, 0, 0, 0.06);
    color: var(--clr-accent-400);
    position: relative;
  }

  .blog-content blockquote::after {
    content: url("/blog/quote.png");
    position: absolute;
    right: 0.1rem;
    bottom: -0.8rem;
  }

  .blog-content h2 {
    font-weight: var(--fw-700);
    font-size: var(--fs-550);
  }

  .blog-content ul {
    margin-left: 1.0625rem;
  }

  .blog-content li {
    margin: 1rem 0;
  }

  .blog-content img {
    width: 100%;
    border-radius: var(--radius-600);
  }

  .img-gallery {
    display: flex;
    width: 100%;
    gap: 1.5rem;
  }

  .bottom-stats {
    margin-top: 1.25rem;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }

  .tags {
    list-style: none;
    display: flex;
    flex-wrap: wrap;
    gap: 0.625rem;
  }

  .tags li {
    padding: 0.5rem 0.875rem;
    background: #f5f5f5;
    transition: 0.3s;
  }

  .tags li:hover {
    background: var(--clr-accent-400);
    color: #fff;
  }

  @media screen and (max-width: 75em) {
    .img-wrapper {
      margin: 0;
    }
  }

  @media screen and (max-width: 62em) {
    .article-container {
      margin-top: 3rem;
      margin-bottom: 5rem;
    }

    .img-gallery {
      flex-wrap: wrap;
    }
  }
</style>

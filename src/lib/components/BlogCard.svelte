<script lang="ts">
  export let blog: {
    image: {
      alt: string;
      src: string;
    };
    title: string;
    category: string;
    date: Date;
  };
</script>

<div {...$$restProps} class="card">
  <a class="image-link" href="/blogs/introduction-to-typescript">
    <img alt={blog.image.alt} class="image" src={blog.image.src} />
  </a>

  <div class="description">
    <a class="category" href="/blogs/introduction-to-typescript">
      <svg
        class="icon icon-tabler icon-tabler-tag"
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
          d="M8.5 8.5m-1 0a1 1 0 1 0 2 0a1 1 0 1 0 -2 0m-3.5 -1.5v3.859c0 .537 .213 1.052 .593 1.432l8.116 8.116a2.025 2.025 0 0 0 2.864 0l4.834 -4.834a2.025 2.025 0 0 0 0 -2.864l-8.117 -8.116a2.025 2.025 0 0 0 -1.431 -.593h-3.859a3 3 0 0 0 -3 3z"
        />
      </svg>
      <span>{blog.category}</span>
    </a>
    <header>
      <a class="title" href="/blogs/introduction-to-typescript"> <h3>{blog.title}</h3></a>
    </header>

    <div class="stats">
      <div class="date-stat">
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
            d="M4 5m0 2a2 2 0 0 1 2 -2h12a2 2 0 0 1 2 2v12a2 2 0 0 1 -2 2h-12a2 2 0 0 1 -2 -2zm12 -4l0 4m-8 -4l0 4m-4 4l16 0m-9 4l1 0l0 3"
          />
        </svg>
        {blog.date.toLocaleDateString()}
      </div>

      <a class="readmore-btn" href="/blogs/introduction-to-typescript">
        Read More

        <svg
          class="icon icon-tabler icon-tabler-arrow-narrow-right"
          fill="none"
          height="24"
          stroke="currentColor"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          viewBox="0 0 24 24"
          width="24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path d="M0 0h24v24H0z" fill="none" stroke="none" />
          <path d="M5 12l14 0m-4 4l4 -4m-4 -4l4 4" />
        </svg>
      </a>
    </div>
  </div>
</div>

<style>
  .card {
    background: white;
    border-radius: var(--radius-400);
    transition: 0.4s;
      border: 1px solid #eee;
  }

  .card:hover {
    box-shadow: 0 10px 30px rgb(0 0 0 / 6%);
  }

  .card:hover .image {
    transform: scale(1.1);
  }

  .title:hover {
    color: var(--clr-accent-400);
  }

  .image-link {
    display: block;
    border-radius: var(--radius-300);
    border-top-left-radius: var(--radius-400);
    border-top-right-radius: var(--radius-400);
    overflow: hidden;
  }

  .image {
    width: 100%;
    aspect-ratio: 16 / 12;
    overflow: hidden;
    object-fit: cover;
    transition: 0.4s;
  }

  .description {
    padding: 1.875rem;
    display: flex;
    flex-direction: column;
    gap: 1.25rem;
  }

  .title {
    font-weight: var(--fw-700);
    color: var(--clr-heading);
    line-height: 1.7;
    font-size: 1.3rem;
    text-decoration: none;
    transition: color 0.2s;
  }

  .stats {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
  }

  .date-stat {
    display: flex;
    gap: 0.3rem;
    align-items: center;
  }

  .readmore-btn {
    font-weight: var(--fw-700);
    align-self: flex-start;
    display: flex;
    align-items: center;
    gap: 0.25rem;
    background: linear-gradient(currentColor 0 0) var(--p, 0) 100% / var(--d, 0)
      3px no-repeat;
    transition: 0.3s, background-position 0s 0.3s;
  }

  .readmore-btn:hover {
    color: var(--clr-accent-400);
    --d: 100%;
    --p: 100%;
  }

  .category {
    display: flex;
    gap: 0.5rem;
    align-items: center;
    color: var(--clr-neutral-400);
    font-weight: var(--fw-600);
  }

  .category svg,
  .category:hover {
    color: var(--clr-accent-400);
  }
</style>

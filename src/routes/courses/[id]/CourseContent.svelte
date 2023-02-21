<script lang="ts">
  import { slide } from "svelte/transition";

  const curriculums = [
    {
      title: "The First Steps",
      modules: [
        "Introduction",
        "Course Overview",
        "Local Development Environment Tools",
      ],
    },
    {
      title: "DataTypes and More",
      modules: ["Introduction", "Course Overview"],
    },
  ];

  let activeCurriculum = -1;
</script>

<section class="course-description">
  <header>
    <h3 class="course-title color-heading">Complete TypeScript Course</h3>
  </header>

  <article>
    <h3>Course Description</h3>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse
      ultrices gravida. Risus commodo viverra maecenas accumsan lacus vel
      facilisis.
    </p>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse
      ultrices gravida. Risus commodo viverra maecenas accumsan lacus vel
      facilisis.
    </p>

    <h3>What You'll Learn From This Course</h3>
    <ul>
      <li>
        Neque sodales ut etiam sit amet nisl purus non tellus orci ac auctor
      </li>
      <li>
        Tristique nulla aliquet enim tortor at auctor urna. Sit amet aliquam id
        diam maer
      </li>
      <li>
        Nam libero justo laoreet sit amet. Lacus sed viverra tellus in hac
      </li>
      <li>
        Tempus imperdiet nulla malesuada pellentesque elit eget gravida cum
        sociis
      </li>
    </ul>

    <h3>Certification</h3>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse
      ultrices gravida. Risus commodo viverra maecenas accumsan lacus vel
      facilisis.
    </p>
  </article>

  <div class="curriculums">
    {#each curriculums as curriculum, index}
      <div class="curriculum" class:active={activeCurriculum === index}>
        <button
          class="curriculumBtn"
          on:click={() =>
            activeCurriculum === index
              ? (activeCurriculum = -1)
              : (activeCurriculum = index)}
        >
          <span>{curriculum.title}</span>

          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="icon icon-tabler icon-tabler-chevron-down"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            stroke-width="2"
            stroke="currentColor"
            fill="none"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <path stroke="none" d="M0 0h24v24H0z" fill="none" />
            <path d="M6 9l6 6l6 -6" />
          </svg>
        </button>

        {#if activeCurriculum === index}
          <div class="modules" transition:slide>
            {#each curriculum.modules as module}
              <ul class="module">
                <li>{module}</li>
              </ul>
            {/each}
          </div>
        {/if}
      </div>
    {/each}
  </div>
</section>

<style>
  article,
  .curriculums {
    padding: 1.875rem;
    border-radius: var(--radius-400);
    border: 1px solid #eee;
  }

  .course-title {
    margin-top: 6rem;
    font-size: var(--fs-700);
    font-weight: var(--fw-800);
  }

  article {
    color: var(--clr-neutral-200);
    margin-top: 2.5rem;
    line-height: 1.6;
  }

  h3,
  .curriculum span {
    font-size: var(--fs-550);
    font-weight: var(--fw-700);
    text-transform: capitalize;
    color: var(--clr-accent-900);
    margin-bottom: 1.25rem;
  }

  .curriculum span {
    margin-bottom: 0;
    font-size: var(--fs-500);
  }

  p {
    margin-bottom: 1.875rem;
  }

  ul {
    margin-left: 1rem;
    margin-bottom: 1.875rem;
  }

  li {
    margin: 0.625rem 0;
  }

  .curriculums {
    margin-top: 2.5rem;
    display: flex;
    flex-direction: column;
    gap: 1.25rem;
  }

  .curriculum {
    border: 1px solid #eee;
    transition: 0.4s;
  }

  .curriculumBtn {
    padding: 0.8125rem 2.1875rem;
    border-radius: var(--radius-400);
    display: flex;
    justify-content: space-between;
    cursor: pointer;
    background: transparent;
    border: none;
    width: 100%;
    align-items: center;
    color: var(--clr-accent-900);
    text-align: left;
  }

  .curriculum.active span,
  .curriculum.active .curriculumBtn {
    color: var(--clr-accent-400);
    transition: 0.3s;
  }

  .icon {
    transition: 0.3s;
  }

  .curriculum.active .icon {
    transform: rotate(180deg);
  }

  .curriculum.active {
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.06);
    border-color: transparent;
  }

  .modules {
    padding: 0 2.1875rem 2.1875rem;
    overflow: hidden;
  }

  .module {
    margin: 0;
    border-bottom: 1px solid #eee;
    padding: 0.875rem 0;
  }

  .module li {
    margin: 0;
  }

  .module:last-child {
    border-bottom: none;
    padding-bottom: 0;
  }

  .modules ul {
    list-style-type: none;
  }

  @media screen and (max-width: 57em) {
    .course-title {
      margin-top: 2rem;
      font-size: var(--fs-600);
    }
  }
</style>

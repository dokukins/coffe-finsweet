<script setup></script>
<template>
  <section class="story">
    <div class="container">
      <div class="story__main">
        <h1 class="heading heading-1">Our Story</h1>
        <p class="text">
          Through True Rich Attended does no end it his mother since favourable
          real had half every him case in packages enquire we up ecstatic.
        </p>
        <div class="story__img">
          <img src="/src/assets/story_image_1.png" alt="" />
          <img src="/src/assets/story_image_2.png" alt="" />
        </div>
      </div>
      <div class="story__text">
        <h4 class="heading heading-4">
          One of the best cafes in <span style="color: #ffb577">New York.</span>
        </h4>
        <p class="text">
          Writing UX copies can be a little frustrating and confusing, and
          sometimes we are unsure about how to get the right word. To crack the
          code for the UX copies, we at Zeta Design wanted to build a Figma
          plugin for the larger design community. The plugin is called the Ghost
          UXWriter and has a set of UX copies cataloged and categorized with a
          voice and tone variation ranging from plain, casual to playful. The
          intention to build this Figma plugin originated from our Medium blog
          post, ‘Designing voice and tone for error messages.
        </p>
        <p class="text">
          Writing UX copies can be a little frustrating and confusing, and
          sometimes we are unsure about how to get the right word. To crack the
          code for the UX copies, we at Zeta Design wanted to build a Figma
          plugin for the larger design community. The plugin is called the Ghost
          UXWriter and has a set of UX copies cataloged and categorized with a
          voice and tone variation ranging from plain, casual to playful. The
          intention to build this Figma plugin originated from our Medium blog
          post, ‘Designing voice and tone for error messages.
        </p>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.story {
  margin-top: 6rem;

  .container {
    display: flex;
    gap: 7rem;
  }

  &__main {
    p {
      margin-top: 1.5rem;
    }
  }

  &__text {
    flex-basis: 100%;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }
  &__img {
    min-width: fit-content;
    display: flex;
    justify-content: space-between;
    img {
      object-fit: contain;
      &:first-child {
        margin-top: 4.5rem;
      }
      &:last-child {
        margin-top: 2rem;
      }
    }
  }
}
</style>

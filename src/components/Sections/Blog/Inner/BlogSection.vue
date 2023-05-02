<script setup>
import PersonItem from "../../PersonItem.vue";
import { useRouter, useRoute } from "vue-router";
const router = useRouter();
const route = useRoute();
</script>

<template>
  <section class="blog">
    <div class="container">
      <div class="blog__header">
        <PersonItem />
        <h1 class="heading heading-1">{{ route.params.name }}</h1>
      </div>
      <img src="/src/assets/blog_inner_bg.png" alt="" />
      <div class="blog__text">
        <h2 class="heading heading-4">
          Edit this text to make it your own. To edit, simply click directly on
          the text.
        </h2>
        <p>
          Writing UX copies can be a little frustrating and confusing, and
          sometimes we are unsure about how to get the right word. To crack the
          code for the UX copies, we at Zeta Design wanted to build a Figma
          plugin for the larger design community. The plugin is called the Ghost
          UXWriter and has a set of UX copies cataloged and categorized with a
          voice and tone variation ranging from plain, casual to playful. The
          intention to build this Figma plugin originated from our Medium blog
          post, ‘Designing voice and tone for error messages.
        </p>
        <p>
          Writing UX copies can be a little frustrating and confusing, and
          sometimes we are unsure about how to get the right word. To crack the
          code for the UX copies, we at Zeta Design wanted to build a Figma
          plugin for the larger design community. The plugin is called the Ghost
          UXWriter and has a set of UX copies cataloged.
        </p>
        <p>
          Writing UX copies can be a little frustrating and confusing, and
          sometimes we are unsure about how to get the right word. To crack the
          code for the UX copies, we at Zeta Design wanted to build a Figma
          plugin for the larger design community. The plugin is called the Ghost
          UXWriter and has a set of UX copies cataloged.
        </p>
        <p>
          Writing UX copies can be a little frustrating and confusing, and
          sometimes we are unsure about how to get the right word. To crack the
          code for the UX copies, we at Zeta Design wanted to build a Figma
          plugin for the larger design community. The plugin is called the Ghost
          UXWriter and has a set of UX copies cataloged and categorized with a
          voice and tone variation ranging from plain, casual to playful. The
          intention to build this Figma plugin originated from our Medium blog
          post, ‘Designing voice.
        </p>
        <p class="heading heading-2">
          Transform Your Idea Into Reality with Ether a Leading Digital Agency
        </p>
        <div>
          <p>
            Step 1: Download the plugin from Figma community, search Ghost
            UXWriter
          </p>
          <p>Step 2: Open the plugin on your artboard</p>
          <p>
            Step 3: Search for your copy or look through the different
            categories of the copies
          </p>
          <p>
            Step 4: Select the type of error you are looking for. You will get
            three different copies for each error
          </p>
          <p>
            Step 5: Tap on the cards to insert text in your frames And you are
            all geared up to make your UX copies more fun and exciting 😎
          </p>
        </div>
        <h3 class="heading heading-4">
          Your own words. You can move the text by dragging and dropping the
          text anywhere on the page.
        </h3>
        <p>
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
.blog {
  &__header {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 3.5rem;
  }

  &__text {
    width: 66%;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  img {
    margin: 5rem 0;
  }
}
</style>

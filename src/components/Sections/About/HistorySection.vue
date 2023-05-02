<script setup>
const moments = [
  {
    year: 1998,
    heading: "Milestone One",
    info: "Through True Rich Attended does no end it his mother since favourable.",
  },
  {
    year: 2005,
    heading: "Milestone Two",
    info: "Through True Rich Attended does no end it his mother since favourable.",
  },
  {
    year: 2012,
    heading: "Milestone Three",
    info: "Through True Rich Attended does no end it his mother since favourable.",
  },
  {
    year: 2021,
    heading: "Milestone Four",
    info: "Through True Rich Attended does no end it his mother since favourable.",
  },
];
</script>
<template>
  <section class="history">
    <div class="container">
      <div class="history__header" id="filter">
        <h2 class="heading heading-1">
          One of the best Cafes in <span>New York</span>
        </h2>
        <p class="text">
          Through True Rich Attended does no end it his mother since favourable
          real had half every him case in packages enquire we up ecstatic..
          Through True Rich Attended does no end it his mother
        </p>
      </div>
      <div class="history__info">
        <h2 class="heading heading-4">Our History</h2>
        <div class="moments">
          <div class="moment" v-for="moment in moments" :key="moment.year">
            <h3 class="heading heading-4">{{ moment.year }}</h3>
            <h4 class="heading heading-2">{{ moment.heading }}</h4>
            <p>
              {{ moment.info }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.history {
  &__header {
    padding: 7.75rem 5rem;
    position: relative;
    background: url("/src/assets/history_bg.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    &::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      background: linear-gradient(
        97.28deg,
        rgba(25, 22, 27, 0.92) 34.6%,
        rgba(25, 22, 27, 0) 83.17%
      );

      width: 100%;
      height: 100%;
    }
    h2,
    p {
      position: relative;
      width: 40%;
    }
    h2 {
      margin-bottom: 1.5rem;
      span {
        color: $info;
      }
    }
  }

  &__info {
    background: $bg-secondary;
    padding: 5rem;
    .moments {
      display: flex;
      gap: 4rem;
      margin-top: 4.5rem;
      padding-top: 2rem;
      border-top: 2px dashed rgba(255, 255, 255, 0.15);
    }

    .moment {
      position: relative;
      display: flex;
      flex-direction: column;
      gap: 1rem;
      h3,
      h4 {
        color: $primary;
      }
      &::before {
        content: "";
        position: absolute;
        top: calc(-3px - 2rem);
        left: 0;
        height: 4px;
        width: 2rem;
        background: $bg-info;
      }
    }
  }
}
</style>

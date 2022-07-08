<template>
  <section class="programs">
    <header>
      <span class="stroke-text">Explore our</span>
      <span>Programs</span>
      <span class="stroke-text">To shape you</span>
    </header>

    <section class="categories-programs">
      <div
        v-for="program, index in programsData"
        :key="index"
        class="category"
      >
        <g
          v-if="program.image"
          v-html="program.image"
        />

        <span>{{ program.heading }}</span>
        <span>{{ program.details }}</span>

        <div class="join-now-category">
          <span>Join Now</span>
          <img
            alt="Arrow Icon"
            src="@/assets/rightArrow.png"
          />
        </div>
      </div>
    </section>
  </section>
</template>

<script>
import { defineComponent } from "vue";
import { programsData } from "@/data/programsData";

export default defineComponent({
  name: "ProgramsSection",

  data () {
    return {
      programsData
    }
  }
})
</script>

<style scoped>
.programs {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  padding: 0 2rem;
}

header {
  color: white;
  font-size: 3rem;
  font-style: italic;
  font-weight: bold;
  text-transform: uppercase;

  display: flex;
  gap: 4rem;
  justify-content: center;
}

.categories-programs {
  display: flex;
  gap: 1rem;
}

.category {
  background-color: gray;
  color: white;

  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 1rem;
  padding: 2rem;
}

.category:hover {
  background: var(--planCard);
  cursor: pointer;
}

.category > :nth-child(1) {
  height: 2rem;
  fill: white;
  width: 2rem;
}

.category > :nth-child(1) > svg {
  height: 100%;
  width: 100%;
}

.category > :nth-child(2) {
  font-size: 1rem;
  font-weight: bold;
}

.category > :nth-child(3) {
  font-size: 0.9rem;
  line-height: 25px;
}

.join-now-category {
  font-weight: bold;

  align-items: center;
  display: flex;
  gap: 2rem;
}

.join-now-category > img {
  width: 1rem;
}
</style>

<template>
  <section class="plans">
    <header class="stroke-header">
      <span class="stroke-text">Ready to start</span>
      <span>Your Journey</span>
      <span class="stroke-text">With us now</span>
    </header>

    <section class="prices-plans">
      <div
        v-for="plan, index in plansData"
        :key="index"
        class="plan"
      >
        <g
          v-if="plan.icon"
          v-html="plan.icon"
        />

        <span>{{ plan.name }}</span>
        <span>$ {{ plan.price }}</span>

        <ul class="features">
          <li
            v-for="feature, index in plan.features"
            :key="index"
          >
            <img
              alt="Check Icon"
              src="@/assets/whiteCheck.png"
            />
            <span>{{ feature }}</span>
          </li>
        </ul>

        <div class="see-more-plan">
          <span>See more benefits →</span>
        </div>

        <button class="btn">
          Join now
        </button>
      </div>
    </section>
  </section>
</template>

<script>
import { defineComponent } from "vue";
import { plansData } from "@/data/plansData";

export default defineComponent({
  name: "PlansSection",

  data () {
    return {
      plansData
    }
  }
})
</script>

<style scoped>
.plans {
  display: flex;
  flex-direction: column;
  gap: 4rem;
  margin-top: -4rem;
  padding: 0 2rem;
  position: relative;
}

.prices-plans {
  display: flex;
  place-content: center;
  gap: 3rem;
}

.plan {
  background-color: var(--caloryCard);
  color: #fff;

  display: flex;
  flex-direction: column;
  gap: 2rem;
  padding: 1.5rem;
  width: 15rem;
}

.plan:nth-child(2) {
  background: var(--planCard);
  transform: scale(1.1);
}

.plan > :nth-child(1) {
  fill: var(--orange);
  height: 2rem;
  width: 2rem;
}

.plan:nth-child(2) > g {
  fill: #fff;
}

.plan > :nth-child(2) {
  font-size: 1rem;
  font-weight: bold;
}

.plan > :nth-child(3) {
  font-size: 3rem;
  font-weight: bold;
}

.plan > :nth-child(5) {
  font-size: 0.8rem;
}

.features {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  list-style: none;
  padding: 0;
}

.features li {
  align-items: center;
  display: flex;
  gap: 1rem;
}

.features li > img {
  width: 1rem;
}

.plan:nth-child(2) > button {
  color: var(--orange);
}
</style>

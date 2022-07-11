<template>
  <section class="reasons">
    <div class="left-reasons">
      <img
        alt="Man training"
        src="@/assets/image1.png"
      />
      <img
        alt="Man training"
        src="@/assets/image2.png"
      />
      <img
        alt="Man training"
        src="@/assets/image3.png"
      />
      <img
        alt="Man training"
        src="@/assets/image4.png"
      />
    </div>

    <div class="right-reasons">
      <h4>Some reasons</h4>

      <h2>
        <span class="stroke-text">Why </span>
        <span>choose us?</span>
      </h2>

      <ul class="list-reasons">
        <li>
          <img
            alt="Check Icon"
            src="@/assets/check.png"
          />
          <p>OVER 140+ EXPERT COACHS</p>
        </li>

        <li>
          <img
            alt="Check Icon"
            src="@/assets/check.png"
          />
          <p>TRAIN SMARTER AND FASTER THAN BEFORE</p>
        </li>

        <li>
          <img
            alt="Check Icon"
            src="@/assets/check.png"
          />
          <p>1 FREE PROGRAM FOR NEW MEMBER</p>
        </li>

        <li>
          <img
            alt="Check Icon"
            src="@/assets/check.png"
          />
          <p>RELIABLE PARTNERS</p>
        </li>
      </ul>

      <span>Our Partners</span>
      <ul class="list-partners">
        <li>
          <img
            alt="New Balance Icon"
            src="@/assets/nb.png"
          />
        </li>
        <li>
          <img
            alt="Adidas Icon"
            src="@/assets/adidas.png"
          />
        </li>
        <li>
          <img
            alt="Nike Icon"
            src="@/assets/nike.png"
          />
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "ReasonsSection"
})
</script>

<style scoped>
.reasons {
  display: flex;
  gap: 2rem;
  padding: 0 2rem;
}

.left-reasons {
  display: grid;
  flex: 1 1;
  gap: 1rem;
  grid-auto-rows: 1fr;
  grid-template-columns: repeat(3, 1fr);
}

.left-reasons > img {
  object-fit: cover;
}

.left-reasons > :nth-child(1) {
  grid-row: 1/3;
  height: 28rem;
  width: 12rem;
}

.left-reasons > :nth-child(2) {
  grid-column: 2/4;
  height: 16rem;
  width: auto;
}

.left-reasons > :nth-child(3) {
  grid-column: 2/3;
  grid-row: 2;
  width: 14rem;
}

.left-reasons > :nth-child(4) {
  grid-column: 3/4;
  grid-row: 2;
  height: 11.2rem;
  width: 10rem;
}

.right-reasons {
  color: white;
  display: flex;
  flex: 1 1;
  flex-direction: column;
  gap: 1rem;
  text-transform: uppercase;
}

.right-reasons > h4 {
  color: var(--orange);
  font-weight: bold;
}

.right-reasons > h2 {
  font-size: 3rem;
  font-weight: bold;
}

.list-reasons,
.list-partners  {
  display: flex;
  flex-direction: column;
  list-style: none;
  padding: 0;
}

.list-reasons > li {
  align-items: center;
  display: flex;
  font-size: 1rem;
  font-weight: bold;
  gap: 1rem;
}

.list-reasons > li > img {
  height: 2rem;
  width: 2rem;
}

.right-reasons > span {
  color: var(--gray);
}

.list-partners {
  flex-direction: row;
  gap: 1rem;
}

.list-partners > li > img {
  width: 2.5rem;
}
</style>

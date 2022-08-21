<template>
<div>
  <section class="timeline-section">
<h2>The Fall of the Jedi</h2>
    <Thefallofthejedi :posts="posts" />
    </section>
    <section class="timeline-section">
      <h2>Age of rebellion</h2>
<Ageofrebellion :posts="posts" />
</section>
</div>
</template>

<script>
export default {
  props: {
    posts: {
      type: Array,
      required: true,
    },
  }
}
</script>

<style>

.release-card {
  border: 1px solid red;
  display: flex;
    justify-content: space-between;
}

.release-title {
  font-size:28px;
}

.release-images {
  max-width: 100px;
}

</style>
<template>
  <ul>
    <li class="release-card" v-for="release of posts" :key="release.slug" v-if="release.era == 'The Fall of the Jedi'">
     <p class="release-title"> {{ release.releasetitle }}</p>
     <p> {{ release.era }} </p>
     <img :src="release.imageurl" :alt="release.releasetitle" class="release-images"/>
    </li>
    </ul>
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
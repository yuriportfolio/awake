<template>
  <generic-card
    :title="title"
    :image="image"
    :link="link"
    :image-dimensions="
      $siteConfig.posts.imageDimensions ||
        $siteConfig.cards.imageDimensions ||
        null
    "
  >
    <span
      v-if="korobka && $siteConfig.posts.displayAuthor"
      class="author-wrapper"
    >
      <strong>Коробка:</strong> {{ korobka }} |
    </span>
  </generic-card>
</template>

<script>
import GenericCard from './GenericCard'

export default {
  components: { GenericCard },
  props: {
    title: {
      type: String,
      default: ''
    },
    image: {
      type: String,
      default: ''
    },
    link: {
      type: String,
      default: ''
    },
    korobka: {		
       type: String,		
       default: ''
  }
  computed: {
   
  }
}
</script>

<template>
  <div class="soup">
    <div class="video" v-if="soup">
      <iframe width="560" height="315" src="https://www.youtube.com/embed/rc43o6q-TqA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
    <div class="soup-button" @click="soup = !soup">🥦</div>
  </div>
</template>

<script>
export default {
  name: 'Soup',
  data: function() {
    return {
      soup: false
    }
  }
}
</script>

<style scoped lang="scss">
@import '../../css/variables.scss';
.soup {
  @media (max-width: $sm) {
    display: none;
  }
}
.video iframe {
  position: fixed;
  bottom: 0;
  right: 0;
}
.soup-button {
  position: fixed;
  bottom: 2rem;
  right: 2rem;
  &:hover {
    cursor: pointer;
  }
}
</style>

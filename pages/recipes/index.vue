<template>
  <section class="recipes">
    <Recipe
      previewText="Awesome chicken"
      title="Delicious Chicken"
      thumbnail="https://s3.ap-northeast-2.amazonaws.com/img.kormedi.com/news/article/__icsFiles/artimage/2016/03/29/c_km601/911811_540.jpg" />

    <Recipe
      previewText="Delicious ramen"
      title="ramen"
      thumbnail="https://img1.daumcdn.net/thumb/R720x0/?fname=https%3A%2F%2Ft1.daumcdn.net%2Fliveboard%2Frealfood%2Fd3d9b8fce02048bfb5564fd1b344f1cb.jpg" />

  </section>
</template>

<script>
import Recipe from '@/components/Recipe'

export default {
  components: {
    Recipe
  }
}

</script>

<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items:center;
}
</style>

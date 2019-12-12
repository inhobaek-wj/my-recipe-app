<template>
  <section class="recipes">
    <Recipe
      v-for="recipe in recipes"
      :key="recipe.id"
      :previewText="recipe.previewText"
      :title="recipe.title"
      :id="recipe.id"
      :thumbnail="recipe.thumbnail" />

  </section>
</template>

<script>
import Recipe from '@/components/Recipe'

export default {
  components: {
    Recipe
  },

  // this allows server side rendering.
  asyncData() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipes: [
            {
              id: 1,
              title: "Delicious Chicken",
              previewText: "Awesome chicken",
              thumbnail: "https://s3.ap-northeast-2.amazonaws.com/img.kormedi.com/news/article/__icsFiles/artimage/2016/03/29/c_km601/911811_540.jpg"
            },
            {
              id: 2,
              title: "Ramen",
              previewText: "Awesome chicken",
              thumbnail: "https://img1.daumcdn.net/thumb/R720x0/?fname=https%3A%2F%2Ft1.daumcdn.net%2Fliveboard%2Frealfood%2Fd3d9b8fce02048bfb5564fd1b344f1cb.jpg"
            }
          ]
        })
      }, 1500)
    })
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

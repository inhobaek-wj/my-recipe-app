<template>
  <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div>
      <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
    </div>
    <p>{{  recipe.description }}</p>
  </section>
</template>

<script>
export default {
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipe: [
            {
              id: "1", /* this should be string */
              title: "Delicious Chicken",
              previewText: "Awesome chicken",
              description: "This is really delicious food",
              thumbnail: "https://s3.ap-northeast-2.amazonaws.com/img.kormedi.com/news/article/__icsFiles/artimage/2016/03/29/c_km601/911811_540.jpg"
            },
            {
              id: "2", /* this should be string */
              title: "Ramen",
              previewText: "Awesome chicken",
              description: "This is really delicious food",
              thumbnail: "https://img1.daumcdn.net/thumb/R720x0/?fname=https%3A%2F%2Ft1.daumcdn.net%2Fliveboard%2Frealfood%2Fd3d9b8fce02048bfb5564fd1b344f1cb.jpg"
            }
          ].find(el => el.id === context.params.id)
        })
      }, 1500)
    })
  }
}
</script>

<style scoped>
.single-recipe {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items:center;
  text-align: center;
  padding: 30px;
}

.recipe-image {
  width: 100%;
}
</style>

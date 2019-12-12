<template>
  <section class="recipes">

    <article class="recipe">
      <div class="thumnail"
           style="background-image: url('https://s3.ap-northeast-2.amazonaws.com/img.kormedi.com/news/article/__icsFiles/artimage/2016/03/29/c_km601/911811_540.jpg')"></div>
      <h1>Title</h1>
      <p>Some nice preview text</p>
    </article>

    <article class="recipe">
      <div class="thumnail"
           style="background-image: url('https://img1.daumcdn.net/thumb/R720x0/?fname=https%3A%2F%2Ft1.daumcdn.net%2Fliveboard%2Frealfood%2Fd3d9b8fce02048bfb5564fd1b344f1cb.jpg')"></div>
      <h1>Title</h1>
      <p>Some nice preview text</p>
    </article>

  </section>
</template>

<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items:center;
}

.recipe {
  box-sizing: border-box;
  width: 280px;
  padding: 8px;
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #aaa;
  margin: 10px;
}

.thumnail {
  background-position: center;
  background-size:cover;
  width: 100%;
  height: 200px;
}
</style>

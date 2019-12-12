<template>
  <section class="recipes">

    <airticle class="recipe">
      <div></div>
      <h1>Title</h1>
      <p>Some nice preview text</p>
    </airticle>

    <airticle class="recipe">
      <div></div>
      <h1>Title</h1>
      <p>Some nice preview text</p>
    </airticle>

  </section>
</template>

<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
}

.recipe {
  box-sizing: border-box;
  width: 280px;
  padding: 8px;
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #aaa;
}
</style>

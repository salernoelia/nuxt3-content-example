<template>
  <main>
    <div class="container">
      <ContentDoc path="/articles/one" class="content" />
    </div>

    <ContentList path="/articles" v-slot="{ list }">
      <div v-for="article in list" :key="article._path">
        <h2 class="content">{{ article.title }}</h2>
        <p class="content">{{ article.description }}</p>
      </div>
    </ContentList>
  </main>
</template>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  font-family: Arial, Helvetica, sans-serif;

  box-sizing: border-box;
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 500px;
  background-color: red;
}

.content {
  align-items: top;
  text-align: left;
  padding: 0 2em;

  img {
    width: 500px;
    object-fit: cover;
    margin-bottom: 1em;
  }

  h1 {
    font-size: 2em;
    margin-bottom: 1em;
    color: #000000;
    font-weight: 600;
  }

  h2 {
    font-size: 1.5em;
    margin-bottom: 1em;
    color: #000000;
    font-weight: 600;
  }

  h3 {
    font-size: 1.2em;
    margin-bottom: 1em;
    color: #000000;
    font-weight: 600;
  }

  a {
    color: #000000;
    text-decoration: none;
  }

  p {
    font-size: 1em;
    margin-bottom: 1em;
    color: #000000;

    width: 200px;
  }
}
</style>

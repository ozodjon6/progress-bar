<template>
  <div id="app">
    <main>
        <div class="navigation">
          <header class="header">
            <h1>Ozodbek Jumaev </h1>
          </header>
          <nav class="main-nav">
            <ul class="main-nav__list">
              <li class="main-nav__item">
                <a href="#" class="main-nav__link">About me</a>
              </li>
              <li class="main-nav__item">
                <a href="#" class="main-nav__link">Contact</a>
              </li>
              <li class="main-nav__item">
                <a href="#" class="main-nav__link">My project</a>
              </li>
              <li class="main-nav__item">
                <a href="#" class="main-nav__link">Life blog</a>
              </li>
            </ul>
          </nav>
        </div>
      <ProgressBar :progress="progress" />
      <Post @progressUpdate="setProgress" />
    </main>
  </div>
</template>

<script>

import Post from "@/components/Post";
import ProgressBar from "@/components/ProgressBar";

export default {
  name: 'App',
  components: {
    Post,
    ProgressBar,
  },
  data() {
    return {
      progress: 0
    }
  },
  methods: {
    setProgress(progress) {
      this.progress = progress
    }
  }
}
</script>

<style>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Roboto, sans-serif;
}

main {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  overflow: hidden;
}

.navigation {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: 10vh;
  padding: 20px;
  background-color: #182E45;
}

header h1 {
  color: #fff;
  font-size: 24px;
}

.main-nav__list {
  margin: 0;
  padding: 0;
  list-style: none;
  display: flex;
  align-items: center;
}

.main-nav__item:not(:last-child) {
  padding-right: 18px;
}

.main-nav__link {
  display: inline-block;
  color: #ffffff;
  text-decoration: none;
}

</style>

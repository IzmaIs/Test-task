<template>
  <div class="main-intro">
    <ul class="intro">
      <li class="intro__items">
        <p id="title">
          ДОБРО ПОЖАЛОВАТЬ В НАШ НОВЫЙ МАГАЗИН!
        </p>
        <p id="main-text">
          Мы садимся вязать, и вселенная вокруг начинает жить по-другому. Точнее, мы создаем
          собственную вселенную, в которой мы отдыхаем, вдохновляемся и создаем шедевры.
          Наш магазин за то, чтобы вы занимались своим любимым делом с удовольствием. Наш
          магазин – это место, где вам предложат пряжу и инструмент исключительного качества
          для создания лучших творений, которые вы только задумали. Наш магазин – это место,
          куда вы просто можете прийти поболтать и выпить чашечку кофе за вязанием
        </p>
        <p id="gyper-text">
          <a href="#">Узнать о нас больше</a>
        </p>
      </li>
      <li class="intro__items">
        <iframe
            class="video-intro"
            width="350"
            height="213"
            src="https://www.youtube.com/embed/C-1aB1KiLmY"
            title="YouTube video player"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
        />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Intro"
}
</script>

<style>
@import "../assets/styles/intro.scss";
</style>
<template>
  <header>
    <div class="top-Head">
      <a href="#" class="Logo"><img src="../../public/imgs/Logo.png" alt="logo"></a>
      <ul class="nav1">
        <li class="nav1__item"><img src="../../public/imgs/Head1.png" alt="Head1"/>
          <p>м. Кропоткинская Соймоновский проезд, д.7 с.1</p></li>
        <li class="nav1__item"><img src="../../public/imgs/Head2.png" alt="Head2"/>
          <p>Пн - Пт 11 - 20 Сб - Вск 11 - 18</p></li>
        <li class="nav1__item"><img src="../../public/imgs/Head3.png" alt="Head3"/>
          <p>+7 800 000 00 +7 800 000 00</p></li>
        <a class="Head4" href="#"><img src="../../public/imgs/Head4.png" alt="Head4"/></a>
      </ul>
      <transition name="fade" mode="out-in">
        <i class="material-icons menu" v-if="!show" @click="switchShow" key="menu">menu</i>
        <i class="material-icons clear" v-else @click="switchShow" key="clear">clear</i>
      </transition>
      <transition name="fade">
        <ul v-if="show" class="menushad">
          <li v-for="item in items" :key="item.name" ><a :href="item.url">{{ item.name }}</a></li>
        </ul>
      </transition>
    </div>
    <div>
    </div>
    <div class="bot-Head">
      <ul class="nav">
        <li class="nav__item" v-for="item in items" :key="item.name"><a :href="item.url" class="nav__link">{{ item.name }}</a></li>
      </ul>
    </div>
  </header>
</template>
<script>

export default {
  data: function () {
    return {
      items: [
        {name: 'Пряжа', url: '#'},
        {name: 'Спицы', url: '#'},
        {name: 'Крючки', url: '#'},
        {name: 'Аксессуары', url: '#'},
        {name: 'Подарочные сертификаты', url: '#'},
        {name: 'МК и описания', url: '#'},
        {name: 'Модели', url: '#'},
      ], show: false
    }
  },
  name: 'TopHead',
  methods: {
    switchShow() {
      this.show = this.show === false;
    }
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/icon?family=Material+Icons");
@import "../assets/styles/headItems01.scss";
</style>

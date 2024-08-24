<template>
  <header class="header">
    <div class="overlay"></div> <!-- Добавляем overlay -->
    <h1>Сайт баскетбольных новостей</h1>
    <p>Добро пожаловать на наш сайт новостей!</p>
  </header>
</template>

<style scoped>
.header {
  position: relative;
  text-align: center;
  padding: 50px 20px; /* Увеличенный padding для лучшего восприятия */
  background-image: url('https://wallpapers.com/images/featured/aesthetic-nba-ba4w0pe75y02ux5q.jpg');
  background-size: cover;
  background-position: center;
  color: white; /* Белый цвет текста для контраста */
  width: 100%; 
  height: 600px;
  margin: 0;
  border: none;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.75); /* Черный overlay с 50% прозрачностью */
  z-index: 1;
}

.header h1, .header p {
  position: relative;
  z-index: 2;
  margin: 0;
}
</style>

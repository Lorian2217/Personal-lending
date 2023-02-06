<template>
  <div class="first_block">
    <p class="textflow">JustSmile</p>
    <p class="copyright" id="copyright">All rights reserved by L.R.N. in 2023 years ©</p>
    <div id="first_quote"> <a @submit.prevent href="#second_block">︾</a>  </div>
  </div>
  <div class="d-flex justify-content-around flex-row p-5 second_block" id="second_block">
    <img src="../assets/ZKnFZb4Wlgk.jpg" class="h-25 w-25 rounded img-fluid" alt="avatar">
    <div class="h-50 w-50 p-2 border border-secondary rounded upper_part">
      <p>Меня зовут Данила Мохнаткин, мне 20 лет, я выпускник гуманитарного колледжа имени святителя Алексия,
      выпустился в 2022 году, со специальностью техник-программист, на текущий момент совершенствуюсь как
      web-разработчик, владею такими языками программирования как Vue.js, PHP, Laravel, MySQL, Html, Css, а также
      имею опыт работы с приложениями: OpenServer, Postman, GitHub, GitHub Desktop, phpMyAdmin, SublimeText,
      Visual Studio Code. <br>
      Уверенный пользователь ПК, умею работать с большей частью приложений Microsoft Office и Libre Office,
      на сегодняшний день обучаюсь в Поволжской православной академии, продолжая развиваться как разработчик.</p>
    </div>
  </div>
</template>

<script>
import { onMounted } from 'vue'

export default{
  name: 'main_page',
  data(){
    return{
     }
  },
  setup(){
    onMounted(() =>{
      console.log('mounted');
      function fadeOut() {
        document.getElementById('first_quote').style.opacity='1';
        console.log('Mounted');
      }
      setTimeout(fadeOut, 800);
    })
  },
  methods:{
  },
  components:{
  }
}
</script>

<style scoped>
/* Первый блок информации */
.first_block{
  min-height: 100vh;
  width: 100%;
  user-select: none;
  background: black;
}
.textflow{
  position: absolute;
  width: inherit;
  top: 50%;
  transform: translateY(-50%);
  margin: auto;
  font-size: 7em;
  background: linear-gradient(90deg, #e933ff, #ffb400, #ff3333, #334dff, #e933ff);
  background-size: 200% auto;
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: textflow 5s linear infinite;
}
@keyframes textflow {
  from {background-position: 200% center}
  to {background-position: 0% center}
}
.copyright{
  color: #c0c0c0;
  position: absolute;
  width: inherit;
  top: 99%;
  transform: translateY(-99%);
  margin: auto;
}
#first_quote{
  font-size: 6em;
  height: 12%;
  color: white;
  position: absolute;
   border: none;
   opacity: 0;
  top: 65%;
  left: 46%;
  right: 46%;
  transform: translateY(-65%);
  transition: all 0.5s;
}
#first_quote:hover{
  transform: translateY(-40%);
  transition: all 0.5s;
}
/* Второй блок информации */
#second_block{
  min-height: 100vh;
  width: 100%;
  user-select: none;
  background: #f2f3f4;
}
.upper_part{
  transition: all 0.5s;
}
.upper_part:hover{
  transform: translateY(5%);
  transition: all 0.5s;
}
.upper_part:valid{
  transform: rotate(45deg);
}

.first_block, #second_block, h3, p, a{
  text-decoration: none;
  color: inherit;
  scroll-behavior: smooth;
}
</style>

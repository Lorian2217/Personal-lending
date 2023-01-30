<template>
  <div class="first_block">
    <!-- <h3>First</h3> -->
    <p class="textflow">JustSmile</p>
    <p class="copyright" id="copyright">All rights reserved by L.R.N. in 2023 years ©</p>
    <p id="first_quote"> ︾ </p>
  </div>
  <div class="second_block" id="second_block">
    <h3>Second</h3>
    <router-link to="/about">About</router-link>
    <h3> {{ this.val }}</h3>
  </div>
</template>

<script>

export default{
  name: 'main_page',
  data(){
    return{
      val: 'Good Day!'
     }
  },
  setup(){
    console.log('Setup');
  },
  methods:{
  },
  mounted(){
    function example() {
      document.getElementById('first_quote').style.opacity='1';
      console.log('Mounted');
    }
    setTimeout(example, 800);
  },
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
  /* display: none; */
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
  transform: translateY(-50%);
  transition: all 0.5s;
}

.second_block{
  min-height: 100vh;
  scroll-behavior: smooth;
  background-color: blue;
  /* border: solid black; */
}

.first_block, .second_block, h3, p{
  margin: inherit;
}
</style>

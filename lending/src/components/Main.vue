<template>
  <div class="first_block">
    <!-- <h3>First</h3> -->
    <p class="textflow">JustSmile</p>
    <p class="copyright" id="copyright">All rights reserved by L.R.N. in 2023 years ©</p>
    <p class="navigation_first"> &#65088; </p>
  </div>
  <div class="second_block" id="second_block">
    <h3>Second</h3>
  </div>
</template>

<script>
export default{
  name: 'main_page',
  data(){
    return{}
  },
  methods:{
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

.navigation_first{
  /* display: none; */
  font-size: 5em;
  height: 10%;
  color: white;
  position: absolute;
  width: inherit;
  top: 65%;
  transform: translateY(-65%);
  margin: auto;
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

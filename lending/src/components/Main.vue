<template>
  <div class="first_block">
    <!-- <h3>First</h3> -->
    <p class="textflow">JustSmile</p>
  </div>
  <div class="second_block">
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
  background: black;
  /* border: solid black; */
}

.textflow{
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

.second_block{
  min-height: 100vh;
  background-color: blue;
  /* border: solid black; */
}

.first_block, .second_block, h3, p{
  margin: inherit;
}
</style>

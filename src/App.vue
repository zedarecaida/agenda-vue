<template>
  <div>
    <Header/>
    <div id="container">
      <PainelContato/>
      <Agenda/>
    </div>
    <Rodape/>
  </div>
</template>

<script>

import Agenda from './components/Agenda.vue'
import PainelContato from './components/PainelContato.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    PainelContato, Header, Agenda, 
  }
}
</script>

<style>
@font-face {
  font-family: "bold";
  src: url(./fonts/KumbhSans-Bold.ttf);
}
@font-face {
  font-family: "padrao1";
  src: url(./fonts/KumbhSans-Regular.ttf);
}


:root {
  --cor-padrao: #0a0a0a;
  --cor-destaque: #9400d3;
  
}
body {
  margin: 0;
  background-color: #fdfdfd;
}
#container{
  display: flex;
  width: 100vw;
  justify-content: space-between;
  margin: auto;
}

@media (max-width: 600px){
  #container{
    display: block;
    padding: auto;
    margin: auto;
  }
  
}
</style>

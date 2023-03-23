
<template>
<div class="app">
<Landingpage @hamburger="sidepanel"/>
  <Costspage/>
  <Propertypage/>
  <Flexibility/>
  <Form />
  <Footer />
  <div class="sidepanel">
    <div class="close" @click="close">X</div>
    <ul class="navigation">
      <li class="menu">Home</li>
      <li class="menu">Landlord</li>
      <li class="menu">Owner</li>
      <li class="menu">Contact Us</li>
    </ul>

  </div>
</div>
  
</template>

<script >
import Propertypage from './components/Propertypage.vue'
import Costspage from './components/Costspage.vue'
import Landingpage from './components/Landingpage.vue'
import Flexibility from './components/Flexibility.vue'
import Form from './components/Form.vue'
import Footer from "./components/Footer.vue"

export default {
  name: 'App',
  components: {
    Landingpage,
    Costspage,
    Propertypage,
    Flexibility,
    Form,
    Footer
  },
  setup(){
    const sidepanel = ()=>{
      const hamburger = document.querySelector('.sidepanel');
      console.log(hamburger);
      hamburger.classList.add('active');
    }
    const close = ()=>{
      const hamburger = document.querySelector('.sidepanel');
      console.log(hamburger);
      hamburger.classList.remove('active');
    }
 
    return{
      sidepanel, close
    }
  }
}

</script>

<style scoped>
.app{
  width: 100%;
  height: 100%;
  position: relative;
  font-family:'Inter';
}
.sidepanel{
  display: none;
}


@media screen and (max-width: 450px ){
.active{
  display: block;
  width: 70%;
  height: 100vh;
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  background: rgb(222, 221, 221);
  padding: 20px;
  transition: 0.5s;
}
.close{
  position: relative;
  top: 0;
  left: 20px;
  font-family: 'Inter', sans-serif;
  color: black;
  font-size: 35px;
  padding: 10px;
  cursor: pointer;
}
.navigation{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  height: 70%;
  width: 100%;
  list-style-type: none;

}
.menu{
  color: black;
  margin-bottom: 10px;
  font-family: 'Inter', sans-serif;
  font-weight: 500;
  font-size: 27px;
  padding: 5px;
  cursor: pointer;
}
}
</style>

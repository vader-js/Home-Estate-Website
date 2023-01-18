<template>
<div class="footerwrapper">
  <div class="footer">
    <div class="footerleft">
        <div class="display">
            <div class="text">{{display.text}}</div>
            <div class="footdetails">
                <img :src="display.image" alt="">
                <span>
                    <p class="name">
                        {{display.name}}
                    </p>
                    <p class="title">
                        {{display.title}}
                    </p>
                </span>
            </div>
            
        </div>
        <div class="radio" @click="handleclick(span)" v-for="span in footerarray" :key="span.text">
            <span>hello</span>
        </div>
    
     
    </div>
    <div class="footerright">
        <img src="../assets/images/videoimage.jpeg" alt="">
        <span></span>
    </div>
  </div>
  <div class="bottom">
    <div class="line"></div>
    <div class="bottomleft">
        <h1>Login</h1>
    </div>
    <div class="bottomright">
        <div class="top">
            <p class="address"> 345 Faulconer Drive, Suite 4 Charllotesville, CA, 12345</p>
        </div>
        <div class="middle">
            <p class="tel">(123)456-7890</p>
            <p class="fax">(123)456-7890</p>
        </div>
        <div class="bottom">
            Social Media
        </div>
    </div>
    <div class="list">
    <div class="line2"></div>
    <nav>
        <ul class="nav">
            <li class="navlist">ABOUT US</li>
            <li class="navlist">CONTACT US</li>
            <li class="navlist">HELP</li>
            <li class="navlist">PRIVACY POLICY</li>
            <li class="navlist">DISCLAIMER</li>
        </ul>
        <p>Copyright &#169; 2020 Minimumlivingcost. All rigth reserved</p>
    </nav>
    </div>
  </div>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity'
import {footer} from "../assets/file.js"
export default {
name: "Footer",
setup(){
    const footerarray = ref(footer);
    const display  = ref(footerarray.value[0]);

    const handleclick = (span)=>{
       if(footerarray.value.includes(span)){
        display.value = span;
       }
    }

    return{ footerarray,  handleclick, display

    }
}
}
</script>

<style scoped>
 .display{
    transition: 1;
}
</style>
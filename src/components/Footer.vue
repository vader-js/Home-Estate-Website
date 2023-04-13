<template>
  <div class="footerwrapper">
    <div class="footer">
      <div class="footerleft">
        <div class="display">
          <div class="text">{{ display.text }}</div>
          <div class="footdetails">
            <img :src="display.image" alt="" />
            <span>
              <p class="name">
                {{ display.name }}
              </p>
              <p class="title">
                {{ display.title }}
              </p>
            </span>
          </div>
        </div>

        <div class="radio">
          <span
            :class="{}"
            @click="handleclick(span)"
            v-for="span in footerarray"
            :key="span.text"
          ></span>
        </div>
      </div>
      <div class="footerright">
        <img src="../assets/images/videoimage.jpeg" alt="" />
        <span class="play"><img src="../assets/images/playbutton.png" alt="play"></span>
      </div>
    </div>
    <div class="line"></div>
    <div class="bottom">
      <section>
      <div class="bottomleft">
        <h1>Login</h1>
      </div>
      <div class="bottomright">
        <aside>
        <div class="top">
          <p class="address">
           <span><img src="../assets/images/Shape.png" alt=""></span> 345 Faulconer Drive, Suite 4 Charllotesville, CA, 12345
          </p>
        </div>
        <div class="middle">
            <p class="tel"><span><img src="../assets/images/Path.png" alt=""></span> (123)456-7890</p>
            <p class="fax"><span><img src="../assets/images/Shape (1).png" alt=""></span>(123)456-7890</p>
        </div>
        <div class="media">
            <p>Social Media</p>
            <div class="socials">
            <span><img src="../assets/images/Instagram-path.png" alt=""></span>
            <span><img src="../assets/images/LinkedIn-path.png" alt=""></span>
            <span><img src="../assets/images/Pinterest.png" alt=""></span>
            <span><img src="../assets/images/Twitter.png" alt=""></span>
            <span><img src="../assets/images/Facebook.png" alt=""></span>
            <span><img src="../assets/images/RSS-path.png" alt=""></span>
        </div>
        </div>
    </aside>
      </div>
    </section>
      <div class="list">
        <div class="line2"></div>
        <nav>
          <ul class="nav">
            <li class="navlist">ABOUT US</li>
            <li class="navlist">CONTACT US</li>
            <li class="navlist">HELP</li>
            <li class="navlist">PRIVACY POLICY</li>
            <li class="navlist">DISCLAIMER</li>
            <li class="emptychild"></li>
            <li>Copyright &#169; 2020 Minimumlivingcost. All rigth reserved</li>
          </ul>
        
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "@vue/reactivity";
import { footer } from "../assets/file.js";
export default {
  name: "Footer",
  setup() {
    const footerarray = ref(footer);
    const display = ref(footerarray.value[0]);

    const handleclick = (span) => {
      if (footerarray.value.includes(span)) {
        display.value = span;
      }
    };

    return { footerarray, handleclick, display };
  },
};
</script>

<style scoped>
.display {
  transition: 0.3s;
  width: 80%;
  height: 50%;
}
.text {
  margin-bottom: 1.5rem;
  width: 100%;
  height: 40%;
}
.footdetails {
  width: 100%;
  height: 40%;
  display: flex;
  align-items: center;
}
.footdetails span {
  margin-left: 1rem;
}
.footdetails img {
  width: 60px;
  height: 60px;
  object-fit: cover;
  border-radius: 50%;
  border: 2px solid #f4511e;
}
.radio {
  display: flex;
  margin-top: 3rem;
}
.radio span {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background-color: #ccc;
}
.radio span:not(:last-child) {
  margin-right: 1rem;
}

.radio span:active {
  background-color: #f4511e;
}
.footer {
  display: flex;
  height: 400px;
  margin-bottom: 7rem;
}
.footerleft {
  flex: 1;
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  background: #f8ebe7;
  width: 100%;
}
.footerright {
  flex: 1;
  width: 100%;
  height: 100%;
  position: relative;
  background: linear-gradient(180deg, rgba(0, 0, 0, 0) 14.58%, rgba(56, 56, 56, 0.84) 100%);
}
.footerright img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  position: inherit;
  z-index: -1;
}
.play{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    width: 80px;
    height: 80px;
    background-color: #f4511e;
    border-radius: 50%;
}
.play img{
    width: 100%;
    height: 100%;
    object-fit: cover;
}
.bottom {
  width: 100%;
  height: 200px;
}
.bottom section {
    display: flex;
    justify-content: center;
    width: 100%;
    height: 100%;
}
.line{
    width: 90%;
    height: 1px;
    background-color: #f4511e;
    margin: 0 auto;
}
.bottomleft, .bottomright{
    flex: 1;
    width: 100%;
    height: 100%;
    display: flex;
    flex-wrap: wrap;
}

.bottomleft h1{
    width: auto;
    height: auto;
   align-self: center;
   margin: 0 auto;
}
.bottomright aside{
    width:80%;
    height:100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    font-size: 14px;
    line-height: 18px;
}
.address{
    width:80%;
    font-size: 14px;
    margin-bottom: 0.3rem;
}
.address span{
    margin-right: 10px;
}
.middle{
    width: 70%;
    display: flex;
    justify-content: space-between;
    margin-bottom: 2rem;
}
.middle span{
margin-right: 10px;
}
.list{
    width: 100%;
    height: 80px;
}
nav{
    width: 80%;
    margin: 0 auto;
    margin-top: 4rem;
}
.nav{
    display: flex;
    justify-content: space-between;
    align-items: center;
    list-style: none;
    font-size: 14px;
    line-height: 18px;
}
.navlist{
    cursor: pointer;
}
.emptychild{
    width: 40px;
}
.media{
    width: 70%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.media p{
    flex: 1;
    color: #0A142F;
    opacity: 0.5;
}
.socials{
    flex: 2;
}
.socials span:not(:last-child){
    margin-right: 10px;
}
@media screen and (max-width: 450px){
  nav{
    width: 90%;
  }
.nav{
  flex-wrap: wrap;
}
.bottomright aside{
  width: 90%;
  flex-wrap: wrap;
}
.bottomright{
   margin: 0 auto;
}
.bottomleft{
  flex: 0.5;
}
}
</style>

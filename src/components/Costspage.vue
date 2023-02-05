<template>
  <div class="costwrapper">
    <div class="heading">
        <h1 class="head">
            Minimum Living Cost Takes Care Of Everything
        </h1>
        <div class="line2"></div>
    </div>
    <div class="costbody">
        <div class="leftbody">
            <img src="../assets/images/costimage.jpeg" alt="terrence">
        </div>
        <div class="rightbody">
        <div class="righttile" v-for="tiles in tile" :key="tiles.description">
            <span class="rightimg"><img :src="tiles.img" alt=""></span> <span class="description">{{tiles.description}}</span>
        </div>
        </div>
    </div>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity'
import { tiles } from "../assets/file.js"
export default {
    name: 'Costpage',
    setup() {
        const tile = ref(tiles)
        const test = ()=>{
            console.log("ayo")
        }
        return {
            tile,test
        }
    }
}
</script>

<style scoped>
.costwrapper{
    width: 100vw;
    height: 100vh;
    background: #E5E5E5;
    padding: 5% 3%;
}
.heading{
    width: 100%;
    margin-bottom: 50px;
}
.line2{
    width: 30%;
    border: 2px solid #F4511E;
    
}
.head{
    font-family: 'Inter';
    font-style: normal;
    font-weight: 800;
    font-size: 36px;
    line-height: 50px;
    width: 70%;
}
.costbody{
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.leftbody{
    flex: 1;
}
.rightbody{
    flex: 2;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    width: 100%;
    padding: 0 3%;
}
.leftbody img{
    width: 380px;
    height: 520px;
    object-fit: cover;
    box-shadow: 5px 24px 53px rgba(0, 0, 0, 0.25);
    border-radius: 50px 0px;
}
.righttile{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    width: 250px;
    justify-content: space-around;
    padding: 20px;
    margin-bottom: 10px;
}
.rightimg{
    width: 77px;
    height: 77px;
    background: #FFFFFF;
    box-shadow: 0px 12px 19px rgba(0, 0, 0, 0.15);
    border-radius: 10px;
    text-align: center;
 
}
.rightimg img{
    margin-top: 15px;
}
.description{
font-family: 'Inter';
font-style: normal;
font-weight: 600;
font-size: 18px;
line-height: 35px;
word-wrap: break-word;
width: 200px;
}
   
@media screen and (max-width: 450px ){
    .costwrapper{
        height: auto;
        position: inherit;
    }
    .costbody{
        display: flex;
        flex-direction: column;
    }
    .head{
        font-size: 25px;
        line-height: 30px;
    }
    .leftbody{
        margin-bottom: 20px;
    }
    .leftbody img{
        width: 280px;
        height: 400px;
    }
    .righttile{
        width: 150px;
        padding: 10px 0;
    }
    .description{
        width: 150px;
    }
}

</style>
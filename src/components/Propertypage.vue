<template>
  <div :class="[viewall ? 'propertywrapper2': 'propertywrapper']">
    <div class="topic">
        <hi class="top">List Of Properties</hi>
        <button class="viewbutton" @click="viewall = !viewall">{{viewall? "collapse": "view all properties"}}</button>
    </div>
    <div class="condition" v-if="!viewall">
    <div class="property" v-for="property in display" :key="property.id">
        <div class="propertyspace">
        <div class="propertyimage">
            <img :src="property.img" alt="">
        </div>
        <div class="propertybody">
            <hi class="location">{{property.location}}</hi>
            <p class="title">{{property.title}}</p>
            <h2 class="price">{{property.cost}}</h2>
            <div class="bottom">
                <span class="phone">{{property.phone}}</span>
                <span class="water">{{property.water}}</span>
                <span class="electricity">{{property.electricity}}</span>
            </div>
        </div>
    </div>
    </div>
    </div>
    <div class="condition" v-else>
    <div class="property" v-for="property in properties" :key="property.id">
        <div class="propertyspace">
        <div class="propertyimage">
            <img :src="property.img" alt="">
        </div>
        <div class="propertybody">
            <h1 class="location">{{property.location}}</h1>
            <p class="title">{{property.title}}</p>
            <h2 class="price">{{property.cost}}</h2>
            <div class="bottom">
                <span class="phone">{{property.phone}}</span>
                <span class="water">{{property.water}}</span>
                <span class="electricity">{{property.electricity}}</span>
            </div>
        </div>
    </div>
    </div>
    </div>
    <footer className="pagination">
    <button @click="handleoperation" :disabled="page <= 1">Prev</button>
    <nav  v-for="n in paginationNumber" :key="n"><button :class="[page == n ? 'pagination-nav': null]" @click="handlepagination(n)">{{n}} </button></nav>
    <button @click="handleoperation" :disabled="page >= 2">Next</button>
    </footer>
  </div>
</template>

<script>
import { property } from "../assets/file.js"
import { ref } from '@vue/reactivity'
import { computed, onMounted } from '@vue/runtime-core';

export default {
    name: 'Propertypage',
    setup() {
        const properties = ref(property);
        const page = ref(0);
        const viewall = ref(false);
        const paginationNumber = ref(Math.ceil(properties.value.length/ 6))
        const handlepagination = (num)=>{
            return page.value = num;
        }
        const handleoperation = (e)=>{
            e.preventDefault();
            switch (e.target.innerHTML) {
                case "Prev":
                    return page.value= page.value - 1;
                case "Next":
                    return page.value= page.value + 1;
                default:
                    return page.value
            }
        }
        const display= computed(()=>{
            return properties.value.slice((6 *(page.value - 1)), (6 * page.value))
        })
        onMounted(()=>{
            return page.value = 1;
        })
        return {
            properties, paginationNumber, handlepagination, display, viewall, handleoperation, page
        }

}
}
</script>

<style scoped>
    .propertywrapper{
        width: 100%;
        height: auto;
        padding: 2%;
        background:#F5F5F5;
    }
    .propertywrapper2{
        height: auto;
        padding: 2%;
        background: white;
    }
    .topic{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
        font-family: 'Inter';
        font-style: normal;
        margin-bottom: 40px;
    }
    .top{
        font-weight: 800;
        font-size: 36px;
        line-height: 50px;
        flex: 3;
        width: 100%;
        position: relative;
    }
    .top::after{
        content: "";
        display: block;
        width: 15%;
        border-bottom: 3px solid #F4511E;
        position: absolute;
        left: 0;
        bottom: -5px;
    }
    .viewbutton{
        flex: 1;
        width: 200px;
        height: 60px;
        background: #F4511E;
        color: white;
        box-shadow: 0px 20px 13px rgba(248, 90, 71, 0.035), 0px 8.14815px 6.51852px rgba(248, 90, 71, 0.0274815), 0px 1.85185px 3.14815px rgba(248, 90, 71, 0.0168519);
        border-radius: 5px;
    }
    .topic button{
        border: none;
        outline: none;
        cursor: pointer;
        font-size: 25px;
    }
    .condition{
        display: flex;
        justify-content: center;
        justify-content: center;
        flex-wrap: wrap;
        width: 100%;
    }
    .property{
        width: 30%;
        height: 450px;
        margin-bottom: 30px;
    }
    .propertyspace{
        width: 300px;
        height: 100%;
        position: relative;
        background: #FFFFFF;
        border: 1px solid #979797;
        border-radius: 26.6166px;
        box-shadow: 0px 34.0693px 36.1986px rgba(0, 0, 0, 0.133714);
    }
    .propertyimage{
        width: 300px;
        height: 250px;
        position: absolute;
        top: 0;
    }
    .propertyimage img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        border-radius: 26.6166px 26.6166px 0px 0px;
    }
    .propertybody{
        width: 100%;
        height: 200px;
        position: absolute;
        bottom: 0;
        padding: 20px;
        font-family: 'DM Sans';
        font-style: normal;
        text-transform: capitalize;
    }
    .location{
        font-weight: 700;
        font-size: 23px;
        line-height: 30px;
        letter-spacing: -0.642075px;
        color: #000000;
    }
    .title{
        font-weight: 400;
        font-size: 18px;
        line-height: 23px;
        letter-spacing: -0.642075px;
        color: #818181;
    }
    .price{
        font-family: 'DM Sans';
        font-style: normal;
        font-weight: 700;
        font-size: 25.552px;
        line-height: 33px;
        letter-spacing: -0.642075px;
        color: #F4511E;
    }
    .bottom{
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px;
        margin-top: 20px;
        border-top: 1px solid #979797;
        width: 100%;
    }
    .bottom span{
        border-right:1px solid #979797 ;
    }
    .pagination{
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        margin-top: 20px;
    }
    .pagination button{
        padding: 10px 15px;
        color: #F4511E;
        font-size: 16px;
        line-height: 24px;
        border-radius: 5px;
        border: .5px solid #ccc;
        outline: none;
    }
    .pagination-nav{
        background: #F4511E;
        color: white !important;
        border-radius: 5px;
    }
    button:disabled{
        color: #979797;
    }
    button:hover{
        color: white;;
        background: #F4511E;
    }
    @media screen and (max-width: 450px) {
        .condition{
            flex-direction: column;
        }
        .property{
            width: 100%;
        }
        .propertyspace{
            margin: 0 auto;
        }
    }
</style>
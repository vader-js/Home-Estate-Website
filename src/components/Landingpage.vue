<template>
  <div class="wrapper">
    <div class="menu"></div>
    <div class="bckimage">
        <img src="../assets/images/background.png" alt="">
    </div>
    <div class="bckwrapper">
    <div class="navigation">
        <div class="logo">
            <img src='../assets/images/logo.png' alt="logo">  
        </div>
        <div class="navigationmenu">
            <ul class="navigationsmenu">
                <li class="menu">Home</li>
                <li class="menu">Landlord</li>
                <li class="menu">Tenants</li>
                <li class="menu">Contact us</li>
            </ul>
        </div>
        <div class="hamburger" @click="$emit('hamburger')">
            <span class="hamburgermenu"></span>
            <span class="hamburgermenu"></span>
            <span class="hamburgermenu"></span>
        </div>
        <div class="empty"></div>
    </div>
    <div class="line"></div>
    <div class="instructions">
        <div class="ad">
             The Most Affordable Place To Stay In The San Francisco Bay Area
        </div>
       <div class="map">
        <div class="maps"></div>
        <div class="direction">
            <div class="directioninput">
                <div class="selecttype">
                    <select name="type" id="type">
                        <option value="landlord">All types</option>
                        <option value="landlord">Landlord</option>
                        <option value="tenant">Tenant</option>
                    </select>
                </div>
                 <div class="selectneihgbourhood">
                    <select name="type" id="type2">
                        <option value="landlord">Neighbourhood</option>
                        <option value="landlord">San Francisco</option>
                        <option value="tenant">New york</option>
                        <option value="tenant">Texas</option>
                    </select>
                </div>
            </div>
        </div>
       </div>
    </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'Landingpage',
   setup(){

    }

}
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,wght@0,400;0,500;0,700;1,400&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,700;1,900&display=swap');

  @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,wght@0,400;0,500;0,700;1,400&family=Inter:wght@300;400;500;600;700;800;900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,700;1,900&display=swap');


.wrapper{
    width: 100%;
    height: 100%;
}
.bckimage{
    background: linear-gradient(200.44deg, rgba(0, 0, 0, 0.0001) 16.41%, rgba(0, 0, 0, 0.51) 77.16%);
    width: 100%;
    height: 100%;
    position: relative;
    top: 0;
    left: 0;
}
.bckimage img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    position: relative;
    z-index: -1;
}
.bckwrapper{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
}
.navigation{
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    padding: 15px 10% 15px 10%;
}
.hamburger{
    display: none;
}
.logo{
   flex: 2;
}
.navigationmenu{
    flex: 3;
    
}
.empty{
    flex: 2;
}
.navigationmenu ul{
    display: flex;
    justify-content: space-between;
    align-items: center;
    list-style-type: none;
}
.navigationmenu ul li{
   font-family: 'DM Sans', sans-serif;
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 16px;
    color: #FFFFFF;
    cursor: pointer;
    padding: 3px;
}
.line{
    width: 80%;
    height: 1px;
    background: #FFFFFF;
    opacity: 0.5;
    margin: 0 auto;
}
.instructions{
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 80%;
    height: 80%;
    margin: 0 auto;
    padding: 10% 0;
}
.ad{
    font-style: normal;
    font-family: 'Inter', sans-serif;
    font-weight: 700;
    font-size: 52px;
    line-height: 70px;
    color: #FFFFFF;
    width: 50%;
}
.map{
    display: flex;
    flex-direction: column;
}
.directioninput{
    display: flex;
    padding: 10px 15px;
    background: #FFFFFF;
    border-radius: 10px;
    align-items: center;
    border: 1px solid rgba(0, 0, 0, 0.2);
    width: 400px;
}
.selecttype{
    padding: 10px;
    background: #F9F9F9;
    width: 130px;
    text-align: center;
    border: 1px solid #E6E6E6;
    border-radius: 5px 0px 0px 5px;
}
.selectneihgbourhood{
    padding: 10px;
    background:#F9F9F9;
    width: 180px;
    text-align: center;
    border: 1px solid #E6E6E6;
    border-radius: 5px 0px 0px 5px;
}
#type{
    border: none;
    outline: none;
    background: transparent;
    font-family: 'Poppins', sans-serif;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 28px;
}
#type2{
    border: none;
    outline: none;
    background: transparent;
    font-family: 'Poppins', sans-serif;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 28px;
}

@media screen and (max-width: 450px ){
.wrapper{
    width: 100vw;
    height: 100vh;
    position: inherit;
}
.bckimage{
    width: 100vw;
    height: 100vh;
}
.bckimage img{
    width: 100%;
    height: 100%;
}
.navigation{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 3%;
}
.line{
    width: 95%;
}
.navigationmenu{
    display: none;
}
.empty{
    display: none;
}
.hamburger{
    display: flex;
    flex-direction: column;
    align-items: flex-end;
}
.hamburgermenu{
    width: 25px;
    height: 3px;
    background-color: white;
    margin-bottom: 5px;
}
.hamburgermenu:nth-child(2){
    width: 30px;
}
.hamburgermenu:nth-child(3){
    width: 20px;
}
.instructions{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.ad{
    font-size: 30px;
    line-height: 40px;
    width: 100%;
}


}
    

</style>
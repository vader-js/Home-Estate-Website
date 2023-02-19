<template>
  <div class="pagewrapper">
    <div class="leftinfo">
      <div class="topimg">
        <div class="firstimg group">
          <img class="first" src="../assets/images/info1.jpeg" alt="" />
          <h2 class="imgh2">Flexible Leases</h2>
        </div>
        <div class="secondimg group">
          <img class="second" src="../assets/images/info2.jpeg" alt="" />
          <h2 class="imgh2">7-Day Happiness Guaranteed</h2>
        </div>
      </div>
      <div class="bottomimg">
        <div class="thirdimg group">
          <img class="third" src="../assets/images/info3.jpeg" alt="" />
          <h2 class="imgh2">Monthly House Cleaning</h2>
        </div>
        <div class="fourthimg group">
          <img class="fourth" src="../assets/images/info4.jpeg" alt="" />
          <h2 class="imgh2">Choose Your Own Roommate</h2>
        </div>
      </div>
    </div>
    <div class="rightinfo">
      <h1 class="flexibilityinfo">
        Flexibility and options to suit your lifestyle
      </h1>
      <p class="flexparagraph">
        You need it? We got it. We make finding your next home easy,
        comfortable, and simple. From our happiness guarantee to our selective
        roomate finder option. We provide you the flexibilty that you most
        desire
      </p>
      <button>Search Rooms</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Flexibility",
};
</script>

<style scoped>
.pagewrapper {
  display: flex;
  align-content: center;
  justify-content: center;
  padding: 3% 5%;
  width: 100%;
  height: 100vh;
}
.leftinfo {
  display: flex;
  flex-direction: column;
  flex: 1;
  width: 100%;
  height: 100%;
  margin-left: 2%;
}
.topimg {
  display: flex;
  justify-content: flex-start;
  align-items: flex-end;
  margin-bottom: 1rem;
}
.firstimg {
  width: 250px;
  height: 334px;
}
.secondimg {
  width: 270px;
  height: 270px;
  margin-left: 1rem;
}
.thirdimg {
  width: 212px;
  height: 285px;
}
.fourthimg {
  width: 338px;
  height: 356px;
  margin-left: 1rem;
}
.group {
  position: relative;
  background: rgba(0, 0, 0, 0.2);
  border-radius: 20px;
}
.imgh2 {
  position: absolute;
  top: 20px;
  left: 25px;
  color: white;
  font-family: "inter";
  font-weight: 600;
  font-size: 24px;
}
.bottomimg {
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
}
img {
  border-radius: 20px;
  object-fit: cover;
  width: 100%;
  height: 100%;
  z-index: -1;
  position: relative;
}

.rightinfo {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 100%;
}
.flexibilityinfo {
  font-family: "inter";
  font-weight: 800;
  font-size: 36px;
  line-height: 50px;
  margin-bottom: 1rem;
  width: 70%;
}
.flexparagraph{
    font-family: 'Inter';
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 32px;
    width: 70%;
    margin-bottom: 1.5rem;
    color: #18191F;
}
.rightinfo button{
    width: 185px;
    height: 63px;
    background: #F4511E;
    border-radius: 13px;
    color: white;
    font-size: 18px;
    font-family: 'Inter';
    font-style: normal;
    line-height: 20px;
    outline: none;
    border: none;
    cursor: pointer;
}
@media screen and (max-width: 450px) {
    .pagewrapper{
        flex-direction: column;
        height: auto;
        margin: 3% 0;
        padding: 2% 3%;
    }
    .rightinfo{
        margin-top: 2rem;
    }
    .leftinfo{
        margin-left: 0;
    }
    .firstimg {
  width: 150px;
  height: 186px;
}
    .secondimg {
  width: 170px;
  height: 170px;
  margin-left: 1rem;
}
    .thirdimg {
  width: 112px;
  height: 185px;
}
    .fourthimg {
  width: 238px;
  height: 256px;
  margin-left: 1rem;
}
.imgh2{
    font-size:18px;
}
    .flexibilityinfo{
        width: 100%;
        font-size: 30px;
    }
    
    .flexparagraph{
        width: 100%;
        font-size: 16px;
    }
    .rightinfo button{
        width: 125px;
        height: 48px;
        font-size: 14px;
    }
}
</style>

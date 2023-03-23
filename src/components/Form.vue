<template>
<h2 class="propertyhead">Your Property With Us And Be Confident That Your Room Will Be Filled Out</h2>
  <form action="">
    <div class="heading">
        <h2>Add A New Property</h2>
    </div>
    <div class="form">
    <label for="name">
        Name <span class="asterick">*</span>
        <input type="text" id="name" placeholder="Enter name" required>
    </label>
    <label for="Address">
        Address <span class="asterick">*</span>
        <input type="text" id="Address" placeholder="Enter Address" required>
    </label>
    <label for="unit">
        Unit Number <span class="asterick">*</span>
        <input type="text" id="unit" placeholder="Enter Unit" required>
    </label>
    <label for="city">
        City <span class="asterick">*</span>
        <select name="city" id="city">
            <option value="">Select City</option>
            <option value="lagos">Lagos</option>
            <option value="abuja">Abuja</option>
            <option value="portharcourt">Port Harcourt</option>
        </select>
    </label>
    <label for="State">
        State <span class="asterick">*</span> 
        <select name="state" id="state">
            <option value="">Select State</option>
            <option value="lagos">Lagos</option>
            <option value="abuja">Abuja</option>
            <option value="portharcourt">Port Harcourt</option>
        </select>
    </label>
    <label for="Room">
        Room Type <span class="asterick">*</span>
        <select name="Room" id="Room">
            <option value="">Select Room Type</option>
            <option value="2 Bedrooms">2 Bedrooms</option>
            <option value="duplex">Duplex</option>
            <option value="penthouse">Penthouse</option>
        </select>
    </label>
    <label for="price">
        Price <span class="asterick">*</span>
        <input type="text" id="price" placeholder="Enter Price" required>
    </label>
    <label for="Room">
        Room Type <span class="asterick">*</span>
        <select name="Room" id="Room">
            <option value="">Select Room Type</option>
            <option value="2 Bedrooms">2 Bedrooms</option>
            <option value="duplex">Duplex</option>
            <option value="penthouse">Penthouse</option>
        </select>
    </label>
    <div></div>
</div>
    <label for="description">
        Description <span class="asterick">*</span>
        <textarea name="description" id="description" cols="70" rows="10" placeholder="Enter Description"></textarea>
    </label>
   <div class="formbottom">
    <h2> Upload Photos </h2>
    <div class="dragndrop">
        <p class="textdirection">
            Drop your images here, or <span><button>browse</button></span>
        </p>
        <p class="supported">supported: JPG,JPEG,PNG</p>
    </div>
   </div>
  <div class="submit"> <input type="submit" class="submit" value="Add New Properties"></div>
  </form>
</template>

<script>
export default {
name: 'Form',
}
</script>

<style scoped>
.propertyhead{
    width: 100%;
    text-align: center;
    font-family: 'Poppins';
    font-weight: 500;
    font-size: 24px;
    line-height: 32px;
    /* margin-bottom: 2rem; */
}
form{
    width: 95%;
    background: #FFFFFF;
    box-shadow: 0px 4px 63px rgba(0, 0, 0, 0.15);
    border-radius: 10px;
    margin: 2rem auto;
    padding: 2%;
    font-family: 'Poppins';
    font-style: normal;
}
.heading{
    width: 100%;
    text-align: center;
    font-weight: 700;
    font-size: 1.2rem;
    line-height: 32px;
    color:  #F4511E;
    margin-bottom: 1rem;
}
.form{
    width: 100%;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
.form label, div{
    flex-basis: 32%;
    width: 100%;
}
 label{
    font-weight: 600;
    font-size: 17px;
    line-height: 24px;
    letter-spacing: 0.2px;
    color: #252B42;
}
.form input, select{
    background: #F9F9F9;
    border: 1px solid #E6E6E6;
    border-radius: 5px;
    width: 100%;
    height: 2.5rem;
    padding: 0 10px;
    margin-bottom: 2rem;
}
input, select, textarea:focus{
    outline: none;
}
.asterick{
    color:  #F4511E;
}
textarea{
    width: 100%;
    background: #F9F9F9;
    border: 1px solid #E6E6E6;
    border-radius: 5px;
    padding: 10px;
    margin-bottom: 1rem;
}
.formbutton{
    width: 100%;
}
.formbutton h2{
    width: 100%;
    text-align: start;
}
.dragndrop{
    background: rgba(244, 81, 30, 0.01);
    border: 1px dashed #F4511E;
    border-radius: 10px;
    height: 7rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    text-align: center;
    font-weight: 500;
}
.textdirection{
font-size: 16px;
line-height: 24px;
}
.textdirection span{
    color: #F4511E;
    
}
.textdirection button{
    background: none;
    border: none;
    color: inherit;
    font-weight: 700;
    font-size: inherit;
}
.supported{
font-size: 12px;
line-height: 18px;
color: rgba(0, 0, 0, 0.5);

}

.submit{
    width: 100%;
   text-align: center;
}
input[type=submit]{
    width: 50%;
    height: 3rem;
    background: #F4511E;
    border-radius: 10px;
    border: none;
    color: #fff;
    font-weight: 700;
    font-size: 16px;
    line-height: 24px;
    letter-spacing: 0.2px;
    margin : 2rem;   
}
@media screen and (max-width: 450px){
    .form label, div{
        flex-basis: 100%;
        width: 100%;
    }
}
    
</style>
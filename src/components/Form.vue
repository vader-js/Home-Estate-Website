<template>
<h2>Your Property With Us And Be Confident That Your Room Will Be Filled Out</h2>
  <form action="">
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
        State <span class="asterick">*</span>
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
        State <span class="asterick">*</span>
        <select name="Room" id="Room">
            <option value="">Select Room Type</option>
            <option value="2 Bedrooms">2 Bedrooms</option>
            <option value="duplex">Duplex</option>
            <option value="penthouse">Penthouse</option>
        </select>
    </label>
    <label for="description">
        Description <span class="asterick">*</span>
        <textarea name="description" id="description" cols="70" rows="10" placeholder="Enter Description"></textarea>
    </label>
   <div class="formbottom">
    <h2>Upload Photos </h2>
    <div class="dragndrop">
        <p class="textdirection">
            Drop your images here, or <span><button>browse</button></span>
        </p>
        <p class="supported">supported: JPG,JPEG,PNG</p>
    </div>
   </div>
   <input type="submit" class="submit" value="Add New Properties">
  </form>
</template>

<script>
export default {
name: 'Form',
}
</script>

<style scoped>

</style>
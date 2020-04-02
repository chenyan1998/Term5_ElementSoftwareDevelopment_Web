<template>
  <card>
    <h5 slot="header" class="title">Edit Your Profile</h5>
    <div class="row">
      <div class="col-md-3 pr-md-1">
        <base-input label="Company "
                  placeholder="Acorn"
                  disabled>
        </base-input>
      </div>
      
      <div class="col-md-2 px-md-1">
        <base-input label="Username"
                  placeholder="chen yan "
                  >
        </base-input>
      </div>

      <div class="col-md-7 pl-md-1">
        <base-input label="Email address"
                  type="email"
                  placeholder="che_yan@email.com">
        </base-input>
      </div>
    </div>

    <div class="row">
      <div class="col-md-6 pr-md-1">
        <base-input label="First Name"
                  
                  placeholder="Chen ">
        </base-input>
      </div>
      <div class="col-md-6 pl-md-1">
        <base-input label="Last Name"
                 
                  placeholder="Yan">
        </base-input>
      </div>
    </div>

    <div class="row">
      <div class="col-md-12">
        <base-input label="Address"
                 
                  placeholder="Home Address">
        </base-input>
      </div>
    </div>

    <div class="row">
      <div class="col-md-4 pr-md-1">
        <base-input label="City"
                 
                  placeholder="Singapore">
        </base-input>
      </div>
      <div class="col-md-4 px-md-1">
        <base-input label="Country"
                  
                  placeholder="Singapore">
        </base-input>
      </div>
      <div class="col-md-4 pl-md-1">
        <base-input label="Postal Code"
                  placeholder="485998">
        </base-input>
      </div>
    </div>


    <div class="row">
      <div class="col-md-8">
        <base-input>
          <label>About Me</label>
          <textarea rows="4" cols="80"
                    class="form-control"
                    placeholder="Here can be your description"
                    >

              </textarea>
        </base-input>
      </div>
    </div>

   
  </card>
</template>
<script>
  export default {
   
  }
</script>
<style>
</style>

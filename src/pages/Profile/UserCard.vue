<template>
  <card type="user">
    <p class="card-text">
    </p>
    
    <div class="author">
      <div class="block block-one"></div>
      <div class="block block-two"></div>
      <div class="block block-three"></div>
      <div class="block block-four"></div>

      <a href="#">
        <img class="avatar" src="img/anime6.png" alt="...">
        <h5 class="title">Chen Yan</h5>
      </a>

      <p class="description">
       Job position 
      </p>
    </div>
    <p></p>
    <p class="card-description">
      <!-- {{user.description}} -->
      My name is Chen Yan , and I’m a third-year 
      ISTD student at SUTD. I am working as a front-end developer in Acorn
    </p>


    <div slot="footer" class="button-container">
      <base-button icon round class="btn-facebook">
        <i class="fab fa-facebook"></i>
      </base-button>
      <base-button icon round class="btn-twitter">
        <i class="fab fa-twitter"></i>
      </base-button>
      <base-button icon round class="btn-google">
        <i class="fab fa-google-plus"></i>
      </base-button>
    </div>

  </card>
</template>
<script>
  export default {
    props: {
      user: {
        type: Object,
        default: () => {
          return {};
        }
      }
    }
  }
</script>
<style>
</style>

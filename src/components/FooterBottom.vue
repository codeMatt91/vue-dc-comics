<template>
  <div class="footer-bottom">
    <div class="container">
      <div id="button">
        <button><a href="#">SIGN-UP NOW!</a></button>
      </div>
      <div id="social">
         <h4>FOLLOW US</h4>
         <ul>
            <li v-for="(immage, index) in immages" :key="index">
               <img :src="require(`../assets/img/footer-${immage.url}`)" alt="immage.description">
            </li>
         </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterBottom",
  data(){
     return {
        immages: [
           {url:"facebook.png", description:"logo facebook"},
           {url:"twitter.png", description:"logo twitter"},
           {url:"youtube.png", description:"logo youtube"},
           {url:"pinterest.png", description:"logo pinterest"},
           {url:"periscope.png", description:"logo periscope"}
        ]
     }
  }
};
</script>

<style lang="scss" scoped>
@import "../assets/sass/_vars.scss";

.footer-bottom {
  display: flex;
  align-items: center;
  position: relative;
  height: 150px;
  background-color: $c-grey;
  z-index: 1;
}

#button {
  display: flex;
  width: 70%;
  button {
     background-color: $c-grey;
     padding: 10px;
     border: 2px solid $c-blue;
     a{
        color: $c-white;
        text-decoration: none;
     }
  }
}

#social{
   display: flex;
   align-items: center;
   ul{
      display: flex;
      li{
         list-style-type: none;
         margin: 5px;
      }
   }
   h4{
      margin-right: 20px;
      color: $c-blue;
   }
}
</style>

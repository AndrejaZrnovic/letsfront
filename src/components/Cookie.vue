<template>
    <div v-if="cookieActivationQuestion" id="cookie"> 
      <div class="d-flex justify-center cookieTape pt-6">
        <h3 class="white--text"><span>We use cookies to personalise content and ads, to provide social media features and to analyse our traffic. </span></h3>
        <v-btn
        class="cookiBtn ml-3"
        @click="cookieAcceptanceQuestion"
        color="primary"
        
        >
          Accept
        </v-btn>
      </div>
    </div>
</template>
<script>
export default {
  name:'Cookie',

  data(){
    return {
      cookieActivationQuestion:true,
      cookieObj:null,
      acceptCookies:'',
    }
  },
  methods: {
    cookieAcceptanceQuestion(){
      if(this.cookieActivationQuestion== true){
        this.cookieObj.create('acceptedCookies','true',10)
        this.checkForThisCookie()
      }
    },

    checkForThisCookie(){
      this.acceptCookies = this.cookieObj.read('acceptedCookies')
      if(!this.acceptCookies){
        this.cookieActivationQuestion = true;
      } else {
        this.cookieActivationQuestion = false;
      }
    }
  },
  mounted() {
    this.cookieObj = new this.$cookie;
    this.checkForThisCookie()
  }
}
</script>
<style scoped lang="scss">

  #cookie {
    position:fixed;
    top:500px;
    left:0;
    width:100%;
    z-index: 3;
  }

  .cookieTape{
      background-color: #292929;
      height:100px;
      

  }


</style>
<template>
  <div class=" d-flex justify-content-between">


      <div>
        <span class="navbutton d-none d-lg-block" @click="navButton()">
          <svg width="1.5em" height="1.5em" viewBox="0 0 16 16" class="bi bi-list" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd" d="M2.5 11.5A.5.5 0 0 1 3 11h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4A.5.5 0 0 1 3 7h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4A.5.5 0 0 1 3 3h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"/>
          </svg>
        </span>
        <span class="navbutton d-lg-none" @click="NavButtonMobile()">
          <svg width="1.5em" height="1.5em" viewBox="0 0 16 16" class="bi bi-list" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd" d="M2.5 11.5A.5.5 0 0 1 3 11h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4A.5.5 0 0 1 3 7h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4A.5.5 0 0 1 3 3h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"/>
          </svg>
        </span>
      </div>

      <div>
        <a href="#"><img src="../assets/logo.png" alt="logo" width="50" height="50"></a>
      </div>

  </div>
</template>

<script>


export default {
  data() {
    return {
      
    }
  },
  methods: {
     navButton() {
       this.emitter.emit('navButton');
    },
    NavButtonMobile(){
      this.emitter.emit('NavButtonMobile')
    }
  },

}
</script>

<style scoped>
 
.navbutton {
    margin-right: 30px;
    margin-top: 10px;
    cursor: pointer;
    opacity: 0.5;
  }
</style>
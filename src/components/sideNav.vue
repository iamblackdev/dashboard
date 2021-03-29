<template>
  <div class="h-100">
        <!-- SIDE BAR HEADER -->
    <div class="sidebar_header" :class="{closeNav: closeNav}" >
      <div>
          <a href="javascript:void(0)" class="closebtn d-lg-none" @click="NavButtonMobile()">&times;</a>
            <div class="side_nav_logo">			
              <a href="#"><img src="../assets/logo.png" alt="logo" width="50" height="50"></a>    
            </div>
      </div>

    </div>
    <!-- SIDE BAR HEADER ENDS -->
    
      <!-- SIDE BAR NAV -->
    <div class="sidebar_nav" :class="{closeNav: closeNav}">

      <ul id="accordion">

        <li class="sidebar_link">
          <div class="tab">
            
            <label class="tab-label" id="headingOne">
              <div data-toggle="collapse" data-target="#collapseOne" aria-expanded="false" aria-controls="collapseOne">
                <span><i class="fa fa-dashboard"></i></span>
                <span class="ml-2 link-name" :class="{removeName: removeName}">Dashboard</span>
              </div>
    
            </label>

            <div class="tab-content collapse" ref="mouseovertab" id="collapseOne" aria-labelledby="headingOne" data-parent="#accordion">
              <ul>
                <li><a href="index.html">Dashboard</a></li>           
              </ul>
            </div>

          </div>
        </li>

        <li class="sidebar_link">
          <div class="tab">
            
            <label class="tab-label" id="headingTwo">
              <div data-toggle="collapse" data-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                <span><i class="fa fa-dashboard"></i></span>
                <span class="ml-2 link-name" :class="{removeName: removeName}">Dashboard</span>
              </div>
    
            </label>

            <div class="tab-content collapse" id="collapseTwo" aria-labelledby="headingTwo" data-parent="#accordion">
              <ul>
                <li><a href="index.html">Dashboard</a></li>           
              </ul>
            </div>

          </div>
        </li>

        <li class="sidebar_link">
          <div class="tab">
            
            <label class="tab-label" id="headingThree">
              <div data-toggle="collapse" data-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                <span><i class="fa fa-dashboard"></i></span>
                <span class="ml-2 link-name" :class="{removeName: removeName}">Dashboard</span>
              </div>
    
            </label>

            <div class="tab-content collapse" id="collapseThree" aria-labelledby="headingThree" data-parent="#accordion">
              <ul>
                <li><a href="index.html">Dashboard</a></li>           
              </ul>
            </div>

          </div>
        </li>
      
      </ul>


    </div>
    <!-- SIDE BAR NAV ENDS -->
  </div>
</template>

<script>

export default {
  
  data() {
    return {
      closeNav: false,
      removeName: false
    }
  },
  methods: {
     NavButtonMobile(){
      this.emitter.emit('NavButtonMobile')
    },
    checkScreenSize(e) {
        if (e.target.innerWidth >= 991) { 
          this.closeNav = false
        }else if (e.target.innerWidth < 991) { 
          this.removeName = false
        }
      }
  },
  created() {
  window.addEventListener("resize", this.checkScreenSize);
  },
   mounted(){
    this.emitter.on('navButton', () => {
      this.closeNav = !this.closeNav
      this.removeName = !this.removeName
    })
    this.emitter.on('NavButtonMobile', () => {
      this.closeNav = !this.closeNav
    })
  },
  destroyed() {
    window.removeEventListener("resize", this.checkScreenSize);
  }
}
</script>

<style scoped>
    /* SIDE BAR STYLE */
  .closebtn {
    position: absolute;
    top: 0;
    right: 35px;
    font-size: 36px;
    margin-left: 50px;
  }
  
  .sidebar_header {
    width: 250px;
    padding-top: 20px;
    text-align: center;
    background: #303641;
    border-bottom: 1px solid #343e50;
    padding-bottom: 20px;
    transition: 0.5s;
  }
  
  .side_nav_logo a img {
    max-width: 120px;
  }
  
  .sidebar_nav {
    width: 250px;
    background: #303641;
    padding-top: 40px;
    transition: 0.5s;
    height: 100%;
  }
  
  .sidebar_nav:hover{
    width: 250px;
  }
   .removeName{
    display: none;
  }
  .sidebar_nav:hover .removeName{
    display: inline-block;
  }
  .closeNav .show {
    display: none ;
  }
  .sidebar_nav:hover .show{
    display: block;
  }

  .tab {
    width: 100%;
    color: white;
    overflow: hidden;
  }
  .sidebar_nav .sidebar_link:hover .tab-label {
    color: white;
  }
  .sidebar_link:hover .tab-label .fa {
    color: white;
  }
  .tab-label {
    padding: 15px 30px;
    cursor: pointer;
    color: #8d97ad;
    transition: color 0.35s ease;
    font-size: 15px;
    text-transform: capitalize;
    width: 100%;
    margin-bottom: 0px;
  }
  .tab-label:hover {
    background: #343942;
  }
  .tab-label .fa {
    transition: color 0.35s ease;
    color: #6a56a5;
  }
  .tab-content {
    color: #8d97ad;
    font-size: 15px;
    margin-left: 40px;
  }
  .tab-content li {
    margin-bottom: 15px;
  }
  .tab-content li:hover {
    color: white;
  }

  .closeNav {
    width: 70px;
  }
  .closeNavMobile{
    width: 0px;
  }
  .remove-header{
    display: none;
  }

   @media (max-width: 991.98px) { 
    .sidebar_header {
      width: 0px;
    }
    .sidebar_nav {
      width: 0px;    
    }
    .closeNav{
      width: 250px;
    }
   }

</style>
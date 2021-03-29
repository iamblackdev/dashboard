<template>
  <div>

     <!-- SIDEBAR STARTS-->
  <div id="mySidenav" class="sidenav">

    <SideNav />
  

  </div>

  <!-- SIDE BAR ENDS -->

     
  <!-- MAIN CONTENT -->

  <div id="main" class="main" :class="{closeMain: closeMain}">
    <!-- HEADER -->
    <div class="container-fluid nav_header">

      <DashboardHeader></DashboardHeader>

    </div>
    <!-- HEADER ENDS -->

     <div class="row classess">
       <div class="col-lg-12 pl-3 pr-5 px-xl-5 pt-4">

				

				<div class="donations">

					<div class="row my-5">

						<div class="col-md-6  ml-3">
							<div class="form-group row">
								<label class="col-form-label font-weight-bold">Filter:</label>
								<div class="ml-3">
								  <input type="text" class="form-control filter-input" placeholder="Type To filter...">
								  <div class="search-icon">
									<i class="fa fa-search"></i>
								  </div>
								</div>
							  </div>
						</div>


						<div class="col-md-3 col-lg-3 col-xl-2 ml-auto">
							<div>
								<span for="exampleFormControlSelect1" class="">Show:</span>
								<select class="select ml-3" id="exampleFormControlSelect1">
								  <option>1</option>
								  <option>2</option>
								  <option>3</option>
								  <option>4</option>
								  <option>5</option>
								</select>
							  </div>
						</div>
					</div>
				</div>
				

				<!-- table -->
				<div class="table-responsive">
					<table class="table text-nowrap">

					  <thead>
						<tr>
						  <td class="table_head  ">
							S.No
							<span class="caret"
							  ><i class="fa fa-caret-up caret_up"></i> <br />
							  <i class="fa fa-caret-down caret_down"></i
							></span>
						  </td>

						  <td class="table_head">
							Growth
							<span class="caret"
							  ><i class="fa fa-caret-up caret_up"></i> <br />
							  <i class="fa fa-caret-down caret_down"></i
							></span>
						  </td>

						  <td class="table_head">
							Transaction id
							<span class="caret"
							  ><i class="fa fa-caret-up caret_up"></i> <br />
							  <i class="fa fa-caret-down caret_down"></i
							></span>
						  </td>

						  <td class="table_head">
							Price
							<span class="caret"
							  ><i class="fa fa-caret-up caret_up"></i> <br />
							  <i class="fa fa-caret-down caret_down"></i
							></span>
						  </td>

						  <td class="table_head">
							Transaction on
							<span class="caret"
							  ><i class="fa fa-caret-up caret_up"></i> <br />
							  <i class="fa fa-caret-down caret_down"></i
							></span>
						  </td>

						  <td class="table_head">
							Status
							<span class="caret"
							  ><i class="fa fa-caret-up caret_up"></i> <br />
							  <i class="fa fa-caret-down caret_down"></i
							></span>
						  </td>

						</tr>
					  </thead>

					  <tbody>

						<tr>
						  <td class="table_row text-center ">1 </td>
						  <td class="table_row">
							<span class="growth">100% Growth</span>
						  </td>
						  <td class="table_row">457874489e</td>
						  <td class="table_row text-right">100</td>
						  <td class="table_row">07-28-2016/16:14:40</td>
						  <td class="table_row">
							  <span class="pending">Pending</span>
						  </td>
						</tr>
						<tr>
						  <td class="table_row text-center">2 </td>
						  <td class="table_row">
							<span class="pending">50% Growth</span>
						  </td>
						  <td class="table_row ">457874489e</td>
						  <td class="table_row text-right">100</td>
						  <td class="table_row">07-28-2016/16:14:40</td>
						  <td class="table_row ">
							  <span class="success">success</span>
						  </td>
						</tr>
						<tr>
						  <td class="table_row text-center">3 </td>
						  <td class="table_row">
							<span class="pending">50% Growth</span>
						  </td>
						  <td class="table_row ">457874489e</td>
						  <td class="table_row text-right">100</td>
						  <td class="table_row">07-28-2016/16:14:40</td>
						  <td class="table_row ">
							  <span class="pending">pending</span>
						  </td>
						</tr>
	
					  </tbody>
					</table>
				  </div>
				  <!-- table ends -->
				  
			  </div>
     </div>
			  <!-- Page content ends -->
   
  </div>
  <!-- MAIN CONTENT ENDS -->
     
  </div>
</template>

<script>
// @ is an alias to /src
import DashboardHeader from '../components/dashboard-header.vue';
import SideNav from '../components/sideNav.vue';

export default {
  name: 'dashboard',
  components: {
    DashboardHeader,
    SideNav
  },
  data() {
    return {
      closeMain: false
    }
  },
  methods: {
      checkScreenSize(e) {
        if (e.target.innerWidth >= 991) { 
           this.closeMain = false
        }
      },
  

  },
  created() {
  window.addEventListener("resize", this.checkScreenSize);
  },
   mounted(){
    this.emitter.on('navButton', () => {
      this.closeMain = !this.closeMain
    })
  },
  destroyed() {
    window.removeEventListener("resize", this.checkScreenSize);
  },
}



</script>
<style scoped>
.sidenav {
    overflow: hidden;
    height: 100%;
    position: fixed;
    z-index: 1;
    top: 0;
    left: 0;
    overflow-x: hidden;
    transition: 0.5s;
  }
  .closeNav {
    width: 70px;
  }
  .closeNavMobile{
    width: 0px;
  }
  .removeName{
    display: none;
  }
  .removeHeader{
    display: none;
  }
  /* MAIN CONTENT STYLES */
  
  .main {
    margin-left: 250px;
    transition: margin-left 0.5s;
  }
  .closeMain {
    margin-left: 70px;
  }
  .nav_header {
    padding: 20px;
    background-color: white;
  }
   

  /* DONATIONS */
  .donations{
  padding-top: 30px;
  padding-left: 10px;
}
.filter-input{
  background-color: white;
  border-color: gray;
  padding-right: 45px;
  color: gray;
}
.filter-input:focus{
  border-color: gray;
}
.search-icon{
  float: right;
  padding-right: 12px;
  position: relative;
  /* left: 200px; */
  top: -31px;
}
.select{
  padding: 5px 10px;
}
.table_head {
  font-size: 18px;
  padding-bottom: 10px;
  position: relative;
}
.caret {
  cursor: pointer;
}
.caret_up {
  position: absolute;
  right: 15px;
}
.caret_down {
  position: absolute;
  top: 24px;
  right: 15px;
}
.table_row {
  font-size: 16px;
  border-bottom: 1px solid rgba(8, 68, 130, 0.1);
}
.growth{
  padding: 5px;
  background-color: #0d83aa;
  color: white;
}
.pending{
  padding: 5px;
  background-color: gray;
  color: white;
}
.success{
  padding: 5px;
  background-color: darkgreen;
  color: white;
}

  @media (max-width: 991.98px) { 
    .classess, bodt, .container{
      overflow-x: hidden !important;
    }
    .sidebar_header {
      width: 0px;
    }
    .sidebar_nav {
      width: 0px;
      
    }
    .closeNav{
      width: 250px;
    }
    .main{
      margin-left: 0px;
    }
   }
</style>
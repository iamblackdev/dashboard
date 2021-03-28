<template>
  <div>

     <!-- SIDEBAR STARTS-->
  <div id="mySidenav" class="sidenav">

    
    <!-- SIDE BAR HEADER -->
    <div class="sidebar_header">
      <div>
          <a href="javascript:void(0)" class="closebtn d-lg-none" @click="NavButtonMobile()">&times;</a>
            <div class="side_nav_logo">			
              <a href="#"><img src="logo.png" alt="logo" width="50" height="50"></a>    
            </div>
      </div>

    </div>
    <!-- SIDE BAR HEADER ENDS -->
    
      <!-- SIDE BAR NAV -->
    <div class="sidebar_nav" >

      <ul id="accordion">
        <li class="sidebar_link">
          <div class="tab">
            
            <label class="tab-label" id="headingOne">
              <div data-toggle="collapse" data-target="#collapseOne" aria-expanded="false" aria-controls="collapseOne">
                <span><i class="fa fa-dashboard"></i></span>
                <span class="ml-2 link-name">Dashboard</span>
              </div>
    
            </label>

            <div class="tab-content collapse " id="collapseOne" aria-labelledby="headingOne" data-parent="#accordion">
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
                <span class="ml-2 link-name">Dashboard</span>
              </div>
    
            </label>

            <div class="tab-content collapse " id="collapseTwo" aria-labelledby="headingTwo" data-parent="#accordion">
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
                <span class="ml-2 link-name">Dashboard</span>
              </div>
    
            </label>

            <div class="tab-content collapse " id="collapseThree" aria-labelledby="headingThree" data-parent="#accordion">
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

  <!-- SIDE BAR ENDS -->

     
  <!-- MAIN CONTENT -->

  <div id="main" class="main">
    <!-- HEADER -->
    <div class="container-fluid d-flex nav_header justify-content-between">

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
    <!-- HEADER ENDS -->

     <div class="row">
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
							  ><i class="fa fa-caret-up caret_up_one"></i> <br />
							  <i class="fa fa-caret-down caret_down_one"></i
							></span>
						  </td>

						  <td class="table_head">
							Growth
							<span class="caret"
							  ><i class="fa fa-caret-up caret_up_two"></i> <br />
							  <i class="fa fa-caret-down caret_down_two"></i
							></span>
						  </td>

						  <td class="table_head">
							Transaction id
							<span class="caret"
							  ><i class="fa fa-caret-up caret_up_three"></i> <br />
							  <i class="fa fa-caret-down caret_down_three"></i
							></span>
						  </td>

						  <td class="table_head">
							Price
							<span class="caret"
							  ><i class="fa fa-caret-up caret_up_four"></i> <br />
							  <i class="fa fa-caret-down caret_down_four"></i
							></span>
						  </td>

						  <td class="table_head">
							Transaction on
							<span class="caret"
							  ><i class="fa fa-caret-up caret_up_five"></i> <br />
							  <i class="fa fa-caret-down caret_down_five"></i
							></span>
						  </td>

						  <td class="table_head">
							Status
							<span class="caret"
							  ><i class="fa fa-caret-up caret_up_six"></i> <br />
							  <i class="fa fa-caret-down caret_down_six"></i
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
							  <span class="success">Pending</span>
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

export default {
  name: 'dashboard',
  data() {
    return {
      
    }
  },
  methods: {
      myEventHandler(e) {
      let sidebar_header = document.querySelector(".sidebar_header")
      let sidebar_nav = document.querySelector(".sidebar_nav")
      let main = document.querySelector(".main")
      let link_name = document.querySelectorAll(".link-name")
      let tab_content = document.querySelectorAll('.tab-content')

        if (e.target.innerWidth >= 991) { 
          sidebar_header.classList.remove('closeNav')
          sidebar_nav.classList.remove('closeNav')
          main.classList.remove('closeMain')
        }else if (e.target.innerWidth < 991) { 
          link_name.forEach(e => {
            e.classList.remove('remove-name')
          })
          tab_content.forEach(e => {
            e.classList.remove('remove-name')
          })
        }
      },
  
    //  FUNCTION FOR NAV BUTTON IN SMALL LAPTOP SCREEN AND ABOVE
     navButton() {

      let sidebar_header = document.querySelector(".sidebar_header")
      let sidebar_nav = document.querySelector('.sidebar_nav')
      let main = document.querySelector(".main")
      let link_name = document.querySelectorAll('.link-name')
      let tab_content = document.querySelectorAll('.tab-content')



      sidebar_header.classList.toggle('closeNav')
      sidebar_nav.classList.toggle('closeNav')

      main.classList.toggle('closeMain')

      link_name.forEach(e => {
        e.classList.toggle('remove-name')
      })
      tab_content.forEach(e => {
        e.classList.toggle('remove-name')
      })

      sidebar_nav.addEventListener('mouseover', e => {
        tab_content.forEach(e => {
          e.classList.remove('remove-name')
        })
      })
    },

    NavButtonMobile(){
      let sidebar_header = document.querySelector(".sidebar_header")
      let sidebar_nav = document.querySelector('.sidebar_nav')
      sidebar_header.classList.toggle('closeNav')
      sidebar_nav.classList.toggle('closeNav')
    }
  },
  created() {
  window.addEventListener("resize", this.myEventHandler);
  },
  destroyed() {
    window.removeEventListener("resize", this.myEventHandler);
  },
}



</script>
<style scoped>
  * {
  margin: 0px;
  padding: 0px;
}
body {
  width: 100%;
  height: 100%;
  outline: none;
  box-sizing: border-box;
  font-family: Arial, Tahoma;
  font-size: 16px;
  color: #000;
  background-color: #fff;
}
*:focus {
  box-shadow: none;
}
input:focus, .custom-select:focus, .form-control:focus {
  box-shadow: none;
}

ul,
li {
  margin: 0;
  padding: 0;
  list-style-type: none;
}
a,
a:hover {
  text-decoration: none;
  color: inherit;
}
/* SIDE BAR STYLE */
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
  .closeNav {
    width: 70px;
  }
  .closeNavMobile{
    width: 0px;
  }
  .sidebar_nav:hover{
    width: 250px;
  }
  .sidebar_nav:hover .remove-name{
    display: inline-block;
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

  .remove-name{
    display: none;
  }
  .remove-header{
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
  .navbutton {
    margin-right: 30px;
    margin-top: 10px;
    cursor: pointer;
    opacity: 0.5;
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
  padding-bottom: 0px;
}
.caret {
  cursor: pointer;
}
.caret_up_one {
  position: relative;
  left: 2px;
  top: -4px;
}
.caret_down_one {
  position: relative;
  left: 47px;
  top: -18px;
}
.caret_up_two {
  position: relative;
  left: 5px;
  top: -4px;
}
.caret_down_two {
  position: relative;
  left: 68px;
  top: -18px;
}
.caret_up_three {
  position: relative;
  left: 2px;
  top: -4px;
}
.caret_down_three {
  position: relative;
  left: 120px;
  top: -18px;
}
.caret_up_four {
  position: relative;
  left: 2px;
  top: -4px;
}
.caret_down_four {
  position: relative;
  left: 48px;
  top: -18px;
}
.caret_up_five {
  position: relative;
  left: 2px;
  top: -4px;
}
.caret_down_five {
  position: relative;
  left: 125.5px;
  top: -18px;
}
.caret_up_six {
  position: relative;
  left: 2px;
  top: -4px;
}
.caret_down_six {
  position: relative;
  left: 58px;
  top: -18px;
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
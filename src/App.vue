<template>
  <!-- <div id="nav">
    <router-link to="/">Dashboard</router-link> |
    <router-link to="/login">Login</router-link> |
    <router-link to="/register">Register</router-link> |
    <router-link to="/forgetpassword">Forget Password</router-link>
  </div> -->
  <router-view/>
</template>

<style>
:root {
  --main-link-color: #8a1717;
  --main-link-hover-color:#f30202e8;
  --primary-color: #546065;
}
body {
  width: 100% !important;
  height: 100% !important; 
  color: #546065;
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.5;
  font-family: 'Montserrat', sans-serif !important;
  background-color: #F6F6F6;
  box-sizing: border-box;
}
*:focus {
  box-shadow: none !important;
  outline: none;
}
.login-form{
  margin-top: 35px;
  background-color: white;
  border-radius: .5rem;
  padding: 40px;
}
.login__header {
    color: #2E384D;
    font-size: 30px;
    font-weight: 600;
    margin-bottom: 10px;
}
.login__sub-header {
    color: #546065;
    font-size: 16px;
    margin-bottom: 20px;
}
.login-btn{
    color: white;
    background-color: var(--main-link-color);
    height: 41px;
    border-radius: 10px;
    text-transform: uppercase;
}
input[type="email"], input[type="password"]{
  font-size: 14px;
}
label{font-size: 14px;}
.have-account{
  font-size: 13px;
}
.have-account .link{
  color: var(--main-link-color);
}
.create-account, .forget-password{
  font-size: 13px;
}
.create-account .link, .forget-password .link{
  color: var(--main-link-color);
}
@media (max-width: 1199.98px) {  }
@media (max-width: 991.98px) { 
  .login-form{
    margin-top: 10px;
  }
 }
@media (max-width: 767.98px) { 
  .login-form{
    padding: 10px;
    background-color: inherit;
  }
  .form-group{
    margin-top: 30px;
 }
}
@media (max-width: 575.98px) {  }


</style>

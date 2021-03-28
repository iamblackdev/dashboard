<template>
  <div id="login">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-md-8 col-lg-5">
          <form class="login-form">
            <h2 class="login__header">Login </h2>
            <p class="login__sub-header">Please enter your credentials to proceed</p>
            <div class="form-group">
                <label for="email">Email Address:</label>
                <input type="email" class="form-control" id="email">
            </div>
            <div class="form-group">
                <label for="password">Password:</label>
                <input type="password" class="form-control mb-3" id="password">
                 <span class="d-block text-right forget-password"><router-link to="/forgetPassword" class="link">Forgot Password?</router-link></span>
            </div>
            
            <button type="submit" class="btn w-100 login-btn">Login</button>

             <div class="text-center mt-4">
                <span class="d-inline-block create-account">Don't Have an account? <router-link class="link"  to="/register">Register</router-link></span>
            </div>

          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'login',
}
</script>

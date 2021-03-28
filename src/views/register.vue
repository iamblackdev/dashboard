<template>
  <div id="login">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-md-8 col-lg-5">
          <form class="login-form">
            <h2 class="login__header">SignUp </h2>
            <p class="login__sub-header">Please enter your credentials to proceed</p>
            <div class="form-group">
                <label for="name">Full Name:</label>
                <input type="text" class="form-control" id="name">
            </div>
            <div class="form-group">
                <label for="password">Password: </label>
                <input type="password" class="form-control" id="password">
            </div>
            <div class="form-group">
                <label for="email">Email Address: </label>
                <input type="email" class="form-control" id="email">
            </div>
            <button type="submit" class="btn w-100 login-btn">Sign up</button>

            <div class="text-center mt-4">
                <span class="d-inline-block create-account">Have an account? <router-link class="link"  to="/login">Login</router-link></span>
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


<template>
  <div id="login">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-md-8 col-lg-5">
          <form class="login-form">
            <h2 class="login__header">Forget Password</h2>
            <p class="login__sub-header">Please provide the email you register with.</p>


                  <div class="form-group">
                    <label for="email">Email Address:</label>
                    <input type="email" class="form-control" id="email">
                </div>
                  <button type="submit" class="w-100 btn login-btn">send reset link</button>

                  <div class="text-center mt-4">
                    <span class="d-inline-block have-account">Have an account already? <router-link class="link"  to="/login">Login</router-link></span>
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

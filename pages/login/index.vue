<template>
  <div class="login-box">
    <div class="login-logo">
      <router-link to="/"><b>Admin</b>LTE </router-link>
    </div>

    <div class="login-box-body">
      <p class="login-box-msg">Sign in to start your session</p>

      <form action="#" method="post">
        <div class="form-group has-feedback">
          <input type="email" class="form-control" placeholder="Email" />
          <span
            class="glyphicon glyphicon-envelope form-control-feedback"
          ></span>
        </div>
        <div class="form-group has-feedback">
          <input type="password" class="form-control" placeholder="Password" />
          <span class="glyphicon glyphicon-lock form-control-feedback"></span>
        </div>
        <div class="row">
          <div class="col-xs-8">
            <label> <input type="checkbox" /> Remember Me </label>
          </div>

          <div class="col-xs-4">
            <button type="submit" class="btn btn-primary btn-block btn-flat">
              Sign In
            </button>
          </div>
        </div>
      </form>

      <div class="social-auth-links text-center">
        <p>- OR -</p>
        <a href="#" class="btn btn-block btn-social btn-facebook btn-flat">
          <i class="fa fa-facebook"></i> Sign in using Facebook
        </a>
        <a href="#" class="btn btn-block btn-social btn-google btn-flat">
          <i class="fa fa-google-plus"></i> Sign in using Google+
        </a>
      </div>

      <a href="#">I forgot my password</a>
      <br />
      <router-link to="/register" class="text-center"
        >Register a new membership</router-link
      >
    </div>
  </div>
</template>
<script>
export default {
  mounted() {
    document.body.classList.remove('skin-blue', 'sidebar-mini')
    document.body.classList.add('hold-transition', 'login-page')
  },
  destroyed() {
    document.body.classList.remove('hold-transition', 'login-page')
    document.body.classList.add('skin-blue', 'sidebar-mini')
  }
}
</script>

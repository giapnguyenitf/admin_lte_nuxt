<template>
  <div class="register-box">
    <div class="register-logo">
      <router-link to="/"><b>Admin</b>LTE</router-link>
    </div>

    <div class="register-box-body">
      <p class="login-box-msg">Register a new membership</p>

      <form action="#" method="post">
        <div class="form-group has-feedback">
          <input type="text" class="form-control" placeholder="Full name" />
          <span class="glyphicon glyphicon-user form-control-feedback"></span>
        </div>
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
        <div class="form-group has-feedback">
          <input
            type="password"
            class="form-control"
            placeholder="Retype password"
          />
          <span class="glyphicon glyphicon-log-in form-control-feedback"></span>
        </div>
        <div class="row">
          <div class="col-xs-8">
            <label>
              <input type="checkbox" /> I agree to the
              <a href="#">terms</a>
            </label>
          </div>

          <div class="col-xs-4">
            <button type="submit" class="btn btn-primary btn-block btn-flat">
              Register
            </button>
          </div>
        </div>
      </form>

      <div class="social-auth-links text-center">
        <p>- OR -</p>
        <a href="#" class="btn btn-block btn-social btn-facebook btn-flat">
          <i class="fa fa-facebook"></i> Sign up using Facebook
        </a>
        <a href="#" class="btn btn-block btn-social btn-google btn-flat">
          <i class="fa fa-google-plus"></i> Sign up using Google+
        </a>
      </div>

      <router-link to="/login" class="text-center"
        >I already have a membership</router-link
      >
    </div>
  </div>
</template>
<script>
export default {
  mounted() {
    document.body.classList.remove('skin-blue', 'sidebar-mini')
    document.body.classList.add('hold-transition', 'register-page')
  },
  destroyed() {
    document.body.classList.remove('hold-transition', 'login-page')
    document.body.classList.add('skin-blue', 'sidebar-mini')
  }
}
</script>

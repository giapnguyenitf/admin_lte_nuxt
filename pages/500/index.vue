<template>
  <div>
    <section class="content">
      <div class="error-page">
        <h2 class="headline text-red">500</h2>

        <div class="error-content">
          <h3>
            <i class="fa fa-warning text-red"></i> Oops! Something went wrong.
          </h3>

          <p>
            We will work on fixing that right away. Meanwhile, you may
            <router-link to="/">return to dashboard</router-link>or try using
            the search form.
          </p>

          <form class="search-form">
            <div class="input-group">
              <input
                type="text"
                name="search"
                class="form-control"
                placeholder="Search"
              />

              <div class="input-group-btn">
                <button
                  type="submit"
                  name="submit"
                  class="btn btn-danger btn-flat"
                >
                  <i class="fa fa-search"></i>
                </button>
              </div>
            </div>
          </form>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  layout: 'Master'
}
</script>

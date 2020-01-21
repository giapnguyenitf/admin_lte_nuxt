<template>
  <div>
    <breadcrumb
      :pageHeader="'Dashboard'"
      :optionalDescription="'Control panel'"
      :level="'Home'"
      :activeLevel="'Dashboard'"
    ></breadcrumb>

    <section class="content">
      <div class="row">
        <div class="col-md-6">
          <div class="box box-primary">
            <div class="box-header with-border">
              <h3 class="box-title">Quick Example</h3>
            </div>
            <form role="form">
              <div class="box-body">
                <div class="form-group">
                  <label for="exampleInputEmail1">Email address</label>
                  <input
                    id="exampleInputEmail1"
                    type="email"
                    class="form-control"
                    placeholder="Enter email"
                  />
                </div>
                <div class="form-group">
                  <label for="exampleInputPassword1">Password</label>
                  <input
                    id="exampleInputPassword1"
                    type="password"
                    class="form-control"
                    placeholder="Password"
                  />
                </div>
                <div class="form-group">
                  <label for="exampleInputFile">File input</label>
                  <input id="exampleInputFile" type="file" />

                  <p class="help-block">Example block-level help text here.</p>
                </div>
                <div class="checkbox">
                  <label> <input type="checkbox" /> Check me out </label>
                </div>
              </div>

              <div class="box-footer">
                <button type="submit" class="btn btn-primary">Submit</button>
              </div>
            </form>
          </div>

          <div class="box box-success">
            <div class="box-header with-border">
              <h3 class="box-title">Different Height</h3>
            </div>
            <div class="box-body">
              <input
                class="form-control input-lg"
                type="text"
                placeholder=".input-lg"
              />
              <br />
              <input
                class="form-control"
                type="text"
                placeholder="Default input"
              />
              <br />
              <input
                class="form-control input-sm"
                type="text"
                placeholder=".input-sm"
              />
            </div>
          </div>

          <div class="box box-danger">
            <div class="box-header with-border">
              <h3 class="box-title">Different Width</h3>
            </div>
            <div class="box-body">
              <div class="row">
                <div class="col-xs-3">
                  <input
                    type="text"
                    class="form-control"
                    placeholder=".col-xs-3"
                  />
                </div>
                <div class="col-xs-4">
                  <input
                    type="text"
                    class="form-control"
                    placeholder=".col-xs-4"
                  />
                </div>
                <div class="col-xs-5">
                  <input
                    type="text"
                    class="form-control"
                    placeholder=".col-xs-5"
                  />
                </div>
              </div>
            </div>
          </div>

          <div class="box box-info">
            <div class="box-header with-border">
              <h3 class="box-title">Input Addon</h3>
            </div>
            <div class="box-body">
              <div class="input-group">
                <span class="input-group-addon">@</span>
                <input
                  type="text"
                  class="form-control"
                  placeholder="Username"
                />
              </div>
              <br />

              <div class="input-group">
                <input type="text" class="form-control" />
                <span class="input-group-addon">.00</span>
              </div>
              <br />

              <div class="input-group">
                <span class="input-group-addon">$</span>
                <input type="text" class="form-control" />
                <span class="input-group-addon">.00</span>
              </div>

              <h4>With icons</h4>

              <div class="input-group">
                <span class="input-group-addon">
                  <i class="fa fa-envelope"></i>
                </span>
                <input type="email" class="form-control" placeholder="Email" />
              </div>
              <br />

              <div class="input-group">
                <input type="text" class="form-control" />
                <span class="input-group-addon">
                  <i class="fa fa-check"></i>
                </span>
              </div>
              <br />

              <div class="input-group">
                <span class="input-group-addon">
                  <i class="fa fa-dollar"></i>
                </span>
                <input type="text" class="form-control" />
                <span class="input-group-addon">
                  <i class="fa fa-ambulance"></i>
                </span>
              </div>

              <h4>With checkbox and radio inputs</h4>

              <div class="row">
                <div class="col-lg-6">
                  <div class="input-group">
                    <span class="input-group-addon">
                      <input type="checkbox" />
                    </span>
                    <input type="text" class="form-control" />
                  </div>
                </div>
                <div class="col-lg-6">
                  <div class="input-group">
                    <span class="input-group-addon">
                      <input type="radio" />
                    </span>
                    <input type="text" class="form-control" />
                  </div>
                </div>
              </div>
            </div>
          </div>
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

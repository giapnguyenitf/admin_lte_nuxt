<template>
  <aside class="main-sidebar">
    <section class="sidebar">
      <div class="user-panel">
        <div class="pull-left image">
          <img
            src="../assets/img/user2-160x160.jpg"
            class="img-circle"
            alt="User Image"
          />
        </div>
        <div class="pull-left info">
          <p>Alexander Pierce</p>
          <a href="#"> <i class="fa fa-circle text-success"></i> Online </a>
        </div>
      </div>

      <form action="#" method="get" class="sidebar-form">
        <div class="input-group">
          <input
            type="text"
            name="q"
            class="form-control"
            placeholder="Search..."
          />
          <span class="input-group-btn">
            <button
              id="search-btn"
              type="submit"
              name="search"
              class="btn btn-flat"
            >
              <i class="fa fa-search"></i>
            </button>
          </span>
        </div>
      </form>

      <ul class="sidebar-menu" data-widget="tree">
        <li class="header">HEADER</li>
        <dropdown-menu :title="'Dashboard'">
          <i slot="icon-menu" class="fa fa-dashboard"></i>
          <li slot="dropdown-item">
            <router-link to="/dashboard-v1">
              <i class="fa fa-circle-o"></i> Dashboard v1
            </router-link>
          </li>
          <li slot="dropdown-item">
            <router-link to="/dashboard-v2">
              <i class="fa fa-circle-o"></i> Dashboard v2
            </router-link>
          </li>
        </dropdown-menu>
        <dropdown-menu :title="'Layout Options'">
          <i slot="icon-menu" class="fa fa-files-o"></i>
          <li slot="dropdown-item">
            <router-link to="/top-navigation">
              <i class="fa fa-circle-o"></i> Top navigation
            </router-link>
          </li>
          <li slot="dropdown-item">
            <router-link to="/boxed">
              <i class="fa fa-circle-o"></i> Boxed
            </router-link>
          </li>
          <li slot="dropdown-item">
            <router-link to="/fixed">
              <i class="fa fa-circle-o"></i> Fixed
            </router-link>
          </li>
          <li slot="dropdown-item">
            <router-link to="/collapse-sidebar">
              <i class="fa fa-circle-o"></i> Collapsed Sidebar
            </router-link>
          </li>
        </dropdown-menu>
        <dropdown-menu :title="'Forms'">
          <i slot="icon-menu" class="fa fa-edit"></i>
          <li slot="dropdown-item">
            <router-link to="/general-elements">
              <i class="fa fa-circle-o"></i> General Elements
            </router-link>
          </li>
          <li slot="dropdown-item">
            <router-link to="/advanced-elements">
              <i class="fa fa-circle-o"></i> Advanced Elements
            </router-link>
          </li>
        </dropdown-menu>
        <menu-item
          :title="'Widgets'"
          :path="'widgets'"
          :classIcon="'fa-th'"
        ></menu-item>
        <dropdown-menu :title="'UI elements'">
          <i slot="icon-menu" class="fa fa-edit"></i>
          <li slot="dropdown-item">
            <router-link to="/general">
              <i class="fa fa-circle-o"></i> General
            </router-link>
          </li>
          <li slot="dropdown-item">
            <router-link to="/icons">
              <i class="fa fa-circle-o"></i> Icons
            </router-link>
          </li>
          <li slot="dropdown-item">
            <router-link to="/buttons">
              <i class="fa fa-circle-o"></i> Buttons
            </router-link>
          </li>
          <li slot="dropdown-item">
            <router-link to="/slider">
              <i class="fa fa-circle-o"></i> Slider
            </router-link>
          </li>
          <li slot="dropdown-item">
            <router-link to="/timeline">
              <i class="fa fa-circle-o"></i> Timeline
            </router-link>
          </li>
          <li slot="dropdown-item">
            <router-link to="/modal">
              <i class="fa fa-circle-o"></i> Modal
            </router-link>
          </li>
        </dropdown-menu>
      </ul>
    </section>
  </aside>
</template>

<script>
import DropdownMenu from '~/components/DropdownMenu/index'
import MenuItem from '~/components/MenuItem/index'

export default {
  components: {
    DropdownMenu,
    MenuItem
  }
}
</script>

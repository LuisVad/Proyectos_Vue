<script setup>

</script>

<template>
  <div id="app">
    <div>
      <b-navbar toggleable="lg" type="dark" variant="dark" sticky>
        <b-navbar-brand href="/inicio"
          ><img
            src="https://placekitten.com/g/30/30"
            class="d-inline-block align-top"
            alt="Kitten"
        /></b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto" right>
            <b-nav-item-dropdown text="Lang" right>
              <b-dropdown-item href="#">EN</b-dropdown-item>
              <b-dropdown-item href="#">ES</b-dropdown-item>
              <b-dropdown-item href="#">RU</b-dropdown-item>
              <b-dropdown-item href="#">FA</b-dropdown-item>
            </b-nav-item-dropdown>

            <b-nav-item-dropdown right>
              <template #button-content>
                <em>User</em>
              </template>
              <b-dropdown-item href="#">Profile</b-dropdown-item>
              <b-dropdown-item href="#">Sign Out</b-dropdown-item>
            </b-nav-item-dropdown>
            <b-breadcrumb :items="items"></b-breadcrumb>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
    <div class="row mt-1">
      <div class="col-3">
        <b-nav vertical class="pt-5 bg-light border-right" variant="pills">
          <b-nav-item class="px-3 py-2">
            <b-link :to="{ name: 'principal' }" class="text-dark">
              <i class="fas fa-edit me-2"></i> Principal
            </b-link>
          </b-nav-item>
          <b-nav-item class="px-3 py-2">
            <b-link :to="{ name: 'formulario' }" class="text-dark">
              <i class="fas fa-edit me-2"></i> Formulario
            </b-link>
          </b-nav-item>
          <b-nav-item class="px-3 py-2">
            <b-link :to="{ name: 'paginacion' }" class="text-dark">
              <i class="fas fa-list-ol me-2"></i> Paginacion
            </b-link>
          </b-nav-item>
        </b-nav>
      </div>
      <div class="col-9">
        <div class="container">
           <navbread></navbread>
          <router-view class="mt-1"></router-view>
        </div>
      </div>
    </div>
  </div>
</template>
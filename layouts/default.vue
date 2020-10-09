<template>
  <div>
    <header>
      <div>
        <b-navbar toggleable="lg">
          <b-navbar-brand href="/">
            Little Message
          </b-navbar-brand>

          <b-navbar-toggle target="nav-collapse" />

          <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav>
              <b-nav-item v-if="$auth.loggedIn" href="#">
                Link
              </b-nav-item>
              <b-nav-item v-if="$auth.loggedIn" href="#" disabled>
                Disabled
              </b-nav-item>
            </b-navbar-nav>

            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto">
              <b-nav-item-dropdown v-if="$auth.loggedIn" right>
                <!-- Using 'button-content' slot -->
                <template v-slot:button-content>
                  <em>User</em>
                </template>
                <b-dropdown-item href="#">
                  Profile
                </b-dropdown-item>
                <b-dropdown-item href="/logout">
                  Sign Out
                </b-dropdown-item>
              </b-nav-item-dropdown>
              <b-nav-item v-else href="/login">
                Sign Up / Log In
              </b-nav-item>
            </b-navbar-nav>
          </b-collapse>
        </b-navbar>
      </div>
    </header>

    <Nuxt />
  </div>
</template>

<style>
html {
  font-size: 16px;
}
</style>

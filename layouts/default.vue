<template>
  <div>
    <header>
      <nav class="navbar navbar-expand-md navbar-light bg-light">
        <NuxtLink class="navbar-brand" to="/">
          Little Message
        </NuxtLink>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarCollapse" aria-controls="navbarCollapse">
          <span class="navbar-toggler-icon" />
        </button>
        <div id="navbarCollapse" class="collapse navbar-collapse">
          <div class="form-inline mt-2 mt-md-0">
            <NuxtLink class="btn btn-outline-primary" to="/login">
              Log In / Sign In
            </NuxtLink>
          </div>
        </div>
      </nav>
    </header>

    <Nuxt />
  </div>
</template>

<style>
html {
  font-size: 16px;
}
</style>

<script>
export default {
    data() {
        return {
            navLinkNames : [
                {
                    label: "Homepage",
                    name: "home"
                },
                {
                    label: "Projects list",
                    name: "projects"
                },
                {
                    label: "About Us",
                    name: "about"
                },
            ]
        }
    },
}
</script>

<template>
<nav class="navbar navbar-expand bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Projects</a>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item" v-for="navItem in navLinkNames">
            <RouterLink class="nav-link" :to="{name: navItem.name}">{{ navItem.label }}</RouterLink>
        </li>
      </ul>
    </div>
  </div>
</nav>
</template>

<style scoped>

</style>
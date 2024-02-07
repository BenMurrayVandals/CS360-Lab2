<template>
  <header class="sticky top-0 flex items-center justify-center gap-x-8 bg-slate-900 p-4 sm:px-6">
    <!-- <NavBarButton data="Home" path="/" />
    <NavBarButton data="About" path="/about" />
    <NavBarButton data="Portfolio" path="/portfolio" />
    <NavBarButton data="Contact" path="/contact" />
    <NavBarButton data="Signin" path="/signin" />
    <NavBarButton data="Signup" path="/signup" /> -->
    <NavBarButton
      v-for="page in pages"
      :data="page"
      :path="`/${page !== 'Home' ? page.toLowerCase() : ''}`"
      :isActivePage="page === activePage"
    />
  </header>
</template>

<script setup lang="ts">
defineProps<{
  activePage: "Home" | "About" | "Portfolio" | "Contact" | "Signin" | "Signup";
}>();

const pages = ["Home", "About", "Portfolio", "Contact", "Signin", "Signup"];
</script>

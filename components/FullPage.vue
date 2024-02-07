<template>
    <div class="flex flex-col h-screen">
    <NavBar :activePage="page" />
    <PageBody :title="page"></PageBody>
    <Footer></Footer>
  </div>
</template>

<script setup lang="ts">
defineProps<{
    page: "Home" | "About" | "Portfolio" | "Contact" | "Signin" | "Signup";
}>()
</script>
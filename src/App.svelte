<script>
  import Home from "./components/home/Home.svelte";
  import Navbar from "./components/navbar/Navbar.svelte";
</script>

<div class="h-full">
  <div>
    <Navbar />
  </div>
  <div class="mx-auto max-w-xl md:max-w-2xl px-3">
    <Home />
  </div>
</div>

<style global>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
  body {
    opacity: 87%;
    color: #ffffff;
    background: #121212;
  }
</style>

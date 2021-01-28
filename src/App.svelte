<script>
  import Header from "./layouts/Header.svelte";
  import Main from "./layouts/Main.svelte";
  import Footer from "./layouts/Footer.svelte";
</script>

<Header />
<div class="pt-10 sm:pt-20 h-full ">
  <Main />
</div>

<!--<Footer />-->
<style global>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
</style>

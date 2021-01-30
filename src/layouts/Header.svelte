<script>
  import { onMount } from "svelte";

  onMount(() => {
    let input_checked = document.getElementById("icon_menu");
    let checked = input_checked.checked;
    isChecked(checked);
  });

  function checked(event) {
    let checked = event.target.checked;
    isChecked(checked);
  }
  function isChecked(checked) {
    console.log(checked);
    let menuOpcion = document.getElementById("list-options");
    checked
      ? menuOpcion.classList.add("list-options-active")
      : menuOpcion.classList.remove("list-options-active");
  }
</script>

<header>
  <nav class="nav bg-blue-700 text-white flex fixed top-0 w-full ">
    <div class=" h-10 sm:h-20 flex items-center justify-center w-full">
      <label for="icon_menu" class="cursor icon-menu">
        <i class="material-icons  md-36">format list bulleted</i>
      </label>
      <input type="checkbox" on:change={checked} id="icon_menu" class="none" />
    </div>
  </nav>
  <div id="list-options" class=" fixed top-0 mt-10  list-options px-5">
    <!--opciones de la navegacion-->
    <ul class="list-options-nav">
      <li><a href="/">Home </a></li>
      <li><a href="/">Featured </a></li>
      <li><a href="/">Recent Projects </a></li>
      <li><a href="/">Presentation </a></li>
      <li><a href="/">Contact </a></li>
    </ul>
  </div>
</header>

<style>
  .nav {
    z-index: 20;
  }
  .icon-menu {
    margin-left: 4rem;
  }
  .list-options-nav li a:hover {
    width: 100%;
    color: darkcyan;
    cursor: pointer;
  }

  .list-options-nav li a {
    padding: 6px 4px;
    text-decoration: none;
  }

  .list-options-nav li {
    background-color: rgb(0, 0, 0, 0.9);
    padding: 6px 10px;
    list-style: none;
    text-align: center;
    border: none;
  }

  .list-options {
    color: white;
    font-family: cursive;
    font-weight: lighter;
    width: 100%;
    transform: translateY(-14rem);
    transition: 0.5s;
    z-index: 10;
  }

  .none {
    display: none;
  }
  .cursor {
    cursor: pointer;
  }
</style>

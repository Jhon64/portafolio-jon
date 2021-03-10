<script>
    import {onMount} from "svelte";
    import {Link,Router} from "svelte-routing"
    onMount(() => {
        /*let input_checked = document.getElementById("icon_menu");
        let checked = input_checked.checked;
        isChecked(checked);*/
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

    export let url = ""
</script>

<header>
    <!-- <nav class="nav bg-blue-700 text-white  fixed top-0 w-full
   sm:block sm:w-20">
       <div class="sm:hidden h-10  flex items-center justify-center w-full">
         <label for="icon_menu" class="cursor icon-menu">
           <i class="material-icons  md-36">format list bulleted</i>
         </label>
         <input type="checkbox" on:change={checked} id="icon_menu" class="none" />
       </div>
       <div class="sm:block">
         <ul>
           <li><a></a></li>
         </ul>
       </div>
     </nav>
     <div id="list-options" class="sm: fixed top-0 mt-10  list-options px-5">-->
    <!--opciones de la navegacion-->
    <!--<ul class="list-options-nav">
      <li><a href="/">Home </a></li>
      <li><a href="/">Featured </a></li>
      <li><a href="/">Recent Projects </a></li>
      <li><a href="/">Presentation </a></li>
      <li><a href="/">Contact </a></li>
    </ul>
  </div>-->
    <nav class="sidebar">
        <div class="sidebar-logo">
            <div class="sidebar-logo__card">
                Sen<em>tra</em>
            </div>
        </div>
        <div class="sidebar-items">

                <ul class="sidebar-items-list">
                    <li class="font-extralight"><a class="sidebar-items-list__link" href="index#home">Home</a></li>
                    <li class="font-extralight"><a class="sidebar-items-list__link" href="index#featured">Featured</a></li>
                    <li class="font-extralight"><a class="sidebar-items-list__link" href="index#recent">Recent Work</a></li>
                    <li class="font-extralight"><a class="sidebar-items-list__link" href="index#presentation">Presentation</a></li>
                    <li class="font-extralight"><a class="sidebar-items-list__link" href="index#blog">Blog</a></li>
                    <li class="font-extralight"><a class="sidebar-items-list__link" href="index#contact">Contact</a></li>
                </ul>

        </div>
    </nav>
</header>

<style>
    .sidebar {
        width: 15rem;
        background-color: rgba(12, 12, 12, 1);
        height: 100%;
        position: fixed;
        top: 0;
        left: 0;
        z-index: 15;
    }

    .sidebar-logo {
        background-color: lightseagreen;
        height: 15%;
        padding: 1rem;
    }

    .sidebar-logo__card {
        border: 2px solid white;
        font-size: 24px;
        font-weight: bold;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        text-transform: uppercase;
        color: white;
    }

    .sidebar-logo__card em {
        font-weight: 100;
        font-style: normal;
    }

    .sidebar-items {
        padding: 2rem 3rem;
    }

    .sidebar-items-list {
        list-style: square;
        color: white;
        padding-top: 30px;
    }

    .sidebar-items-list li {
        padding: 5px;
        font-size: 20px;
    }

    .sidebar-items-list li a {
        text-decoration: none;
        color: white !important;
    }

    .sidebar-items-list__link {
        text-decoration: none;
        color: white !important;
    }

    /*.nav {
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

    .sidebar{
      width: 4rem;
    }
    .none {
      display: none;
    }
    .cursor {
      cursor: pointer;
    }*/
</style>

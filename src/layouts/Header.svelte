<script>
  function checked(event) {
    let checked = event.target.checked;
    let menuOpcion = document.getElementById("list-options");

    if (checked) {
      menuOpcion.classList.add("list-options-active");
    } else {
      menuOpcion.classList.remove("list-options-active");
    }
    console.log(menuOpcion);
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
      <li><a>Home </a></li>
      <li><a>Featured </a></li>
      <li><a>Recent Projects </a></li>
      <li><a>Presentation </a></li>
      <li><a>Contact </a></li>
    </ul>
  </div>
</header>

<style>
  .nav {
    z-index: 10;
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
    padding: 4px;
    text-decoration: none;
  }

  .list-options-nav li {
    background-color: rgba(0, 0, 0, 0.4);
    padding: 5px 10px;
    list-style: none;
    text-align: center;
    border: none;
  }

  .list-options {
    color: white;
    font-family: cursive;
    font-weight: lighter;
    width: 100%;
    transform: traslateY(0);
    transition: 0.7s;
  }

  .none {
    display: none;
  }
  .cursor {
    cursor: pointer;
  }
</style>

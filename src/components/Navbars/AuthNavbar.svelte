<script>
  import { link } from "svelte-routing";

  // core components
  import PagesDropdown from "components/Dropdowns/PagesDropdown.svelte";

  let navbarOpen = false;

  function setNavbarOpen() {
    navbarOpen = !navbarOpen;
  }
</script>

<nav
  class="top-0 absolute z-50 w-full flex flex-wrap items-center justify-between px-2 py-3 navbar-expand-lg"
>
  <div
    class="flex flex-col lg:flex-row list-none lg:ml-auto"
  >
    <div
      class="w-full relative flex justify-between lg:w-auto lg:static lg:block lg:justify-start"
    >
    <b><h1>Book my dine
      </h1>
    </b>
     
    </div>
    <div
      class="lg:flex flex-grow items-center bg-white lg:bg-opacity-0 lg:shadow-none rounded shadow-lg {navbarOpen ? 'block':'hidden'}"
      id="example-navbar-warning"
    >
      <!-- <ul class="flex flex-col lg:flex-row list-none mr-auto">
        <li class="flex items-center">
          <a
            class="lg:text-white lg:hover:text-blueGray-200 text-blueGray-700 px-3 py-4 lg:py-2 flex items-center text-xs uppercase font-bold"
            href="https://www.creative-tim.com/learning-lab/tailwind/svelte/overview/notus?ref=ns-auth-navbar"
          >
            <i
              class="lg:text-blueGray-200 text-blueGray-400 far fa-file-alt text-lg leading-lg mr-2"
            />
            Docs
          </a>
        </li>
      </ul> -->
      <ul class="flex flex-col lg:flex-row list-none lg:ml-auto">
        <li class="flex items-center">
          <PagesDropdown />
        </li>
      
        <li class="flex items-center">
          <button
            class="bg-white text-blueGray-700 active:bg-blueGray-50 text-xs font-bold uppercase px-4 py-2 rounded shadow hover:shadow-md outline-none focus:outline-none lg:mr-1 lg:mb-0 ml-3 mb-3 ease-linear transition-all duration-150"
            type="button"
          >
            Registration
          </button>
        </li>
      </ul>
    </div>
  </div>
</nav>

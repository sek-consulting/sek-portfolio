<script>
  let showMenu = false;

  let links = [
    { url: "#about", text: "About Us" },
    { url: "#contact", text: "Contact" },
  ];
</script>

<header
  class="absolute top-0 z-20 w-full bg-zinc-100 text-zinc-800 dark:bg-zinc-800 dark:text-zinc-100"
>
  <nav
    class="container mx-auto py-4 px-6 md:flex md:h-20 md:items-center md:justify-between md:p-2"
  >
    <div class="flex items-center justify-between">
      <a href="#/">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 752 500"
          class="w-16 fill-current"
        >
          <path
            d="M.3.3h311.535v108.24H.3V.3Zm0 392.055v107.641h311.535V392.355H.3Zm135.47-87.75V196.381h221.613L553.425.3h150.982L399.431 304.605H135.77Zm328.098 60.976 76.997-75.731 211.132 210.146H598.698l-134.83-134.415Z"
          />
        </svg>
      </a>
      <button class="flex md:hidden" on:click={() => (showMenu = !showMenu)}>
        <svg viewBox="0 0 100 80" class="h-6 w-6 fill-current">
          <rect y="0" width="100" height="14" rx="7" />
          <rect y="33" width="100" height="14" rx="7" />
          <rect y="66" width="100" height="14" rx="7" />
        </svg>
      </button>
    </div>

    <ul
      id="nav-links"
      class="mt-8 flex-col items-center space-y-4 text-lg md:mt-0 md:flex md:flex-row md:space-y-0 md:space-x-10 
      {showMenu ? 'flex' : 'hidden'}"
    >
      {#each links as link}
        <li>
          <a href={link.url}>{link.text}</a>
        </li>
      {/each}
    </ul>
  </nav>
</header>

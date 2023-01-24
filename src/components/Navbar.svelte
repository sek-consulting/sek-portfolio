<script>
  let showMenu = false;

  let links = [
    { url: "/#services", text: "Services" },
    { url: "/#about", text: "About Us" },
    { url: "/blog", text: "Blog" },
  ];
</script>

<header
  class="absolute top-0 z-20 w-full bg-zinc-100 text-zinc-800 dark:bg-zinc-800 dark:text-zinc-100"
>
  <nav
    class="container mx-auto py-4 px-6 md:flex md:h-20 md:items-center md:justify-between md:p-2"
  >
    <div class="flex items-center justify-between">
      <a href="/#">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 60 40"
          class="h-10 fill-current"
        >
          <path
            d="M0 0h24.971v8.644H0V0Zm0 31.388v8.611h24.971v-8.611H0Zm10.872-7.02V15.71h17.747L44.318 0h12.091L31.986 24.368H10.872Zm26.274 4.878 6.166-6.12L60.22 39.999H47.944L37.146 29.246Z"
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

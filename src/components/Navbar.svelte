<script>
let showMenu = false;

let links = [
    {url: "#about", text: "About Us"},
]
</script>

<header class="absolute top-0 w-full text-zinc-100 z-20">

    <nav class="container mx-auto py-4 px-6 md:h-20 md:p-2 md:flex md:items-cemter md:justify-between">
        
        <div class="flex items-center justify-between">
            <a href="#/" class="hover:text-sky-400">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 752 500" class="w-16 fill-current">
                    <path d="M.3.3h311.535v108.24H.3V.3Zm0 392.055v107.641h311.535V392.355H.3Zm135.47-87.75V196.381h221.613L553.425.3h150.982L399.431 304.605H135.77Zm328.098 60.976 76.997-75.731 211.132 210.146H598.698l-134.83-134.415Z"></path>
                </svg>  
            </a>
            <button class="flex md:hidden" on:click={() => showMenu = !showMenu}>
                <svg viewBox="0 0 100 80" class="w-6 h-6 fill-current">
                    <rect y="0" width="100" height="14" rx="7"></rect>
                    <rect y="33" width="100" height="14" rx="7"></rect>
                    <rect y="66" width="100" height="14" rx="7"></rect>
                </svg>    
            </button>
        </div>

        <ul id="nav-links" class="flex-col items-center mt-8 space-y-4 md:flex md:flex-row md:mt-0 md:space-y-0 md:space-x-10 text-lg {
            showMenu ? 'flex' : 'hidden'
        }">
            {#each links as link}
                <li>
                    <a href={link.url} class="hover:text-sky-400">{link.text}</a>
                </li>
            {/each}
            <li>
                <a href="https://www.instagram.com/e.k_fotos" target="_blank" rel="noreferrer" class="hover:text-sky-400">
                    <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
                        <path d="M7.8 2h8.4C19.4 2 22 4.6 22 7.8v8.4a5.8 5.8 0 0 1-5.8 5.8H7.8C4.6 22 2 19.4 2 16.2V7.8A5.8 5.8 0 0 1 7.8 2m-.2 2A3.6 3.6 0 0 0 4 7.6v8.8C4 18.39 5.61 20 7.6 20h8.8a3.6 3.6 0 0 0 3.6-3.6V7.6C20 5.61 18.39 4 16.4 4H7.6m9.65 1.5a1.25 1.25 0 0 1 1.25 1.25A1.25 1.25 0 0 1 17.25 8A1.25 1.25 0 0 1 16 6.75a1.25 1.25 0 0 1 1.25-1.25M12 7a5 5 0 0 1 5 5a5 5 0 0 1-5 5a5 5 0 0 1-5-5a5 5 0 0 1 5-5m0 2a3 3 0 0 0-3 3a3 3 0 0 0 3 3a3 3 0 0 0 3-3a3 3 0 0 0-3-3Z"></path>
                    </svg>
                </a>
            </li>

        </ul>

    </nav>

</header>

<style type="text/postcss">
 /* do local tailwind stuff here */
</style>
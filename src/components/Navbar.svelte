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
        </ul>

    </nav>

</header>

<style type="text/postcss">
 /* do local tailwind stuff here */
</style>
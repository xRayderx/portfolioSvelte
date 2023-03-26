<script lang="ts">
    let showMenu = false;

    function handleMenuClick() {
        showMenu = !showMenu;
    }
</script>

<header class="z-30 fixed flex items-center w-full h-14 sm:h-16">
    <div class="container flex items-center justify-between px-6 mx-auto">
        <div class="flex items-center text-3xl font-bold text-gray-700 uppercase">
            <a href="/" class="mt-1 ml-3 text-lg">
                jose martinez
            </a>
        </div>

        <div class="flex items-center">
            <nav class="lg:flex items-center text-lg text-gray-800 uppercase {showMenu ? 'block' : 'hidden'}">
                <a href="/skills" class="flex px-6 py-2 hover:text-blue-400">skills</a>
                <a href="/projects" class="flex px-6 py-2 hover:text-blue-400">projects</a>
                <a href="/education" class="flex px-6 py-2 hover:text-blue-400">education</a>
            </nav>
            <button on:click={handleMenuClick} class="flex flex-col ml-4 lg:hidden">
                <span class="w-6 h-1 mb-1 bg-gray-800"></span>
                <span class="w-6 h-1 mb-1 bg-gray-800"></span>
                <span class="w-6 h-1 mb-1 bg-gray-800"></span>
            </button>
        </div>
    </div>
</header>

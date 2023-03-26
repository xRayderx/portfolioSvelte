<script lang="ts">
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();

    function handleClick() {
        dispatch('click');
    }
</script>

<button on:click={handleClick} class="w-1/3 bg-blue-600 rounded-lg h-10 border-2 p-2 flex items-center justify-center">
    Contactame
</button>
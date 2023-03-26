<script lang="ts">
    import BtnContact from "../lib/components/btnContact.svelte";
    import BtnCV from "../lib/components/btnCV.svelte";
    import ModalContact from "../lib/components/ModalContact.svelte";
    /*import Hero from "assets/jmcv.png";*/

    let showModal = false;

    function handleButtonClick(){
        showModal = true;
    }

    function handleModalSubmit(e){
        console.log(e.detail);
        showModal = false;
    }

</script>

{#if showModal}
    <ModalContact on:submit={handleModalSubmit}/>
{/if}

<section class="py-20 text-white bg-black">
    <div class="max-w-screen-xl mx-auto">
        <div class="flex items-center space-x-4">
            <div class="flex flex-col w-1/2">
                <div class="flex flex-col space-y-4">
                    <h1>Jose Martinez</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet nobis harum cum cupiditate ipsa odit qui autem, debitis fugiat voluptas repellat maiores tempora obcaecati excepturi sint ratione nemo maxime? Nostrum!</p>
                </div>
                <div class="flex mt-12 space-x-3 flex-col sm:flex-row sm:items-center gap-4">
                    <BtnContact on:click={handleButtonClick}/>
                    <BtnCV/>
                </div>
            </div>
            <div class="w-1/2">
                <!--<img src={Hero} alt="profile hero" class="w-full h-full">-->
            </div>
        </div>
    </div>
</section>
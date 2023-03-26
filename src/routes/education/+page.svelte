<script lang="ts">
    
    let education = [
      {
        grado: 'Bachiller en Ciencias',
        instituto: 'Liceo Oswaldo Torres Viña',
        año: '2008-2013',
      },
      {
        grado: 'Ingeniero de Sistemas',
        instituto: 'I.U.P Santiago Mariño',
        año: '2013-Current',
      },
      // Add more education here
    ];
</script>
  
<section id="education" class="bg-gray-100 p-4">
    <div class="container mx-auto">
      <h2 class="text-2xl font-bold mb-4">My Education</h2>
      <ul>
        {#each education as item}
          <li class="mb-4">
            <h3 class="text-lg font-semibold">{item.grado}</h3>
            <p>{item.instituto}</p>
            <p>{item.año}</p>
          </li>
        {/each}
      </ul>
    </div>
</section>
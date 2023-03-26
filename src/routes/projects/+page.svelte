<script lang="ts">
     let projects = [
    {
      title: 'Project 1',
      description: 'Lorem ipsum dolor sit amet...',
      image: '/images/project1.jpg',
    },
    {
      title: 'Project 2',
      description: 'Lorem ipsum dolor sit amet...',
      image: '/images/project2.jpg',
    },
    // Add more projects here
  ];
</script>

<section id="projects" class="bg-white p-4">
    <div class="container mx-auto">
      <h2 class="text-2xl font-bold mb-4">My Projects</h2>
      <ul class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
        {#each projects as project}
          <li>
            <div class="rounded shadow overflow-hidden">
              <img src={project.image} alt={project.title} class="w-full" />
              <div class="p-4">
                <h3 class="text-lg font-semibold mb-2">{project.title}</h3>
                <p>{project.description}</p>
              </div>
            </div>
          </li>
        {/each}
      </ul>
    </div>
</section>
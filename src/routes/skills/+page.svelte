<script lang="ts">
    let skills = [
    { name: 'HTML', experience: 'Basics and fundamentals' },
    { name: 'CSS', experience: 'Vanilla, SASS' },
    { name: 'JavaScript', experience: 'Vanilla, Typescript' },
    { name: 'Frameworks', experience: 'React, Vue, Svelte' },
  ];
</script>

<section id="skills" class="bg-gray-100 p-4">
    <div class="container mx-auto">
      <h2 class="text-2xl font-bold mb-4">My Skills</h2>
      <ul>
        {#each skills as skill}
          <li class="mb-4">
            <div class="flex justify-between items-center mb-1">
              <span>{skill.name}</span>
              <span>{skill.experience}</span>
            </div>
            <div class="w-full h-2 bg-gray-300 rounded-full overflow-hidden">
              <div
                class="h-full bg-green-500"
                style="--w: {skill.experience}%; width: var(--w)"
              />
            </div>
          </li>
        {/each}
      </ul>
    </div>
</section>
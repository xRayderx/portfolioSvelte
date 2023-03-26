<script lang="ts">
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
  
    let name = '';
    let email = '';
    let message = '';
  
    function handleSubmit(event) {
      event.preventDefault();
      dispatch('submit', { name, email, message });
      name = '';
      email = '';
      message = '';
    }
</script>
  
<div class="fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center" >
    <div class="bg-white rounded shadow p-4 max-w-md w-full">
      <h2 class="text-2xl font-bold mb-4">Contact Me</h2>
      <form on:submit|preventDefault={handleSubmit}>
        <div class="mb-4">
          <label for="name" class="block text-sm font-semibold mb-1">
            Name
          </label>
          <input
            type="text"
            id="name"
            bind:value={name}
            required
            class="w-full border border-gray-300 rounded px-3 py-2"
          />
        </div>
        <div class="mb-4">
          <label for="email" class="block text-sm font-semibold mb-1">
            Email
          </label>
          <input
            type="email"
            id="email"
            bind:value={email}
            required
            class="w-full border border-gray-300 rounded px-3 py-2"
          />
        </div>
        <div class="mb-4">
          <label for="message" class="block text-sm font-semibold mb-1">
            Message
          </label>
          <textarea
            id="message"
            bind:value={message}
            required
            rows={5}
            class="
              w-full border border-gray-300 rounded px-3 py-2 resize-none leading-snug focus:outline-none focus:ring focus:border-blue-
              300 focus:z-[1]
              "
          />
        </div>
        <button type='submit' class='bg-blue hover:bg-blue-dark text-white font-bold py-2 px-4 rounded'>
            Send Message
        </button> 
      </form>
    </div>
</div>
<script>
  import { fade } from "svelte/transition";
  let visible = false;

  function handleClick() {
    visible = !visible;
  }
</script>

<!-- Navbar goes here -->
<nav class="w-full">
  <div class="mx-auto max-w-6xl px-3">
    <div class="flex justify-between">
      <div class="flex space-x-10 py-2 px-3">
        <!-- logo -->
        <div>
          <!-- svelte-ignore a11y-invalid-attribute -->
          <a href="#" class="flex items-center py-2 px-3 flex-wrap">
            <svg
              class="mr-2 text-white-400  hover:scale-125"
              xmlns="http://www.w3.org/2000/svg"
              x="0px"
              y="0px"
              width="30"
              height="30"
              viewBox="0 0 30 30"
              style=" fill:#bb86fc;"
            >
              <path
                d="M 4.6582031 4 C 3.6182031 6.431 4.0382031 8.4602656 4.4082031 9.5722656 C 2.9152031 11.172266 2.0019531 13.3765 2.0019531 16.3125 C 2.0019531 23.5795 6.5919531 26 15.001953 26 C 23.411953 26 28.001953 23.5795 28.001953 16.3125 C 28.002953 13.4765 27.036656 11.264766 25.472656 9.6347656 C 25.696656 9.2667656 26.003906 8.5485 26.003906 7.1875 C 26.003906 5.1405 25.316406 4 25.316406 4 C 24.247406 4 21.735203 4.4310469 19.658203 6.4980469 C 18.183203 6.1310469 16.610906 6 15.003906 6 C 13.429906 6 11.888406 6.0862969 10.441406 6.4042969 C 10.348406 6.3182969 7.7612031 4 4.6582031 4 z M 10.005859 13.5 C 11.308859 13.514 13.458906 13.999 15.003906 14 C 16.548906 13.999 18.697 13.514 20 13.5 C 22.522 13.5 24 15.502656 24 17.972656 C 24 22.024656 21.656859 23.999 15.005859 24 L 15.003906 24 L 15 24 C 8.349 23.999 6.0058594 22.024656 6.0058594 17.972656 C 6.0058594 15.502656 7.4838594 13.5 10.005859 13.5 z M 10.5 17 A 1.5 2 0 0 0 9 19 A 1.5 2 0 0 0 10.5 21 A 1.5 2 0 0 0 12 19 A 1.5 2 0 0 0 10.5 17 z M 19.5 17 A 1.5 2 0 0 0 18 19 A 1.5 2 0 0 0 19.5 21 A 1.5 2 0 0 0 21 19 A 1.5 2 0 0 0 19.5 17 z"
              /></svg
            >
            <span class="font-bold">Yash Goenka</span>
          </a>
        </div>
        <!-- primary nav -->
        <div class="hidden md:flex items-center space-x-3 ">
          <!-- svelte-ignore a11y-invalid-attribute -->
          <a href="#" class="hover:text-red-900">Home</a>
          <!-- svelte-ignore a11y-invalid-attribute -->
          <a href="#" class="hover:text-red-900">Work</a>
          <!-- svelte-ignore a11y-invalid-attribute -->
          <a href="#" class="hover:text-red-900">Contact</a>
        </div>
      </div>

      <!-- secondary nav -->
      <div class="hidden md:flex items-center">
        <!-- svelte-ignore a11y-invalid-attribute -->
        <a
          href="#"
          class="bg-[#03dac5] hover:bg-yellow-300 text-yellow-900 rounded py-2 px-3 hover:text-black"
          >Download</a
        >
      </div>

      <div class="md:hidden flex items-center">
        <!-- svelte-ignore a11y-invalid-attribute -->
        <button class="flex items-center" on:click={handleClick}>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            />
          </svg>
        </button>
      </div>
    </div>
  </div>

  {#if visible}
    <div class="md:hidden">
      <div class="flex flex-col py-2 px-3 " in:fade={{ delay: 200 }}>
        <!-- svelte-ignore a11y-invalid-attribute -->
        <a href="#" class="hover:text-red-900 py-2 px-3">Home</a>
        <!-- svelte-ignore a11y-invalid-attribute -->
        <a href="#" class=" hover:text-red-900 py-2  px-3">Work</a>
        <!-- svelte-ignore a11y-invalid-attribute -->
        <a href="#" class="hover:text-red-900 py-2  px-3">Contact</a>
      </div>
    </div>
  {/if}
</nav>

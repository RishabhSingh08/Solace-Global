<script>
  import "../app.css";
  import '@fortawesome/fontawesome-free/css/all.min.css'
  import Icon from "../lib/images/SolaceGlobalLogo.png";
    let isDropdownOpen = false;

    function toggleDropdown() {
        isDropdownOpen = !isDropdownOpen;
    }

    function closeDropdown() {
        isDropdownOpen = false;
    }

    
</script>


<main>
  <div class="flex h-full">
    <div class="flex-grow"></div>
      <div class="flex-shrink-0 w-[1200px]">

<nav class="w-full py-4 border-b relative">
    <div class="grid grid-cols-3 items-center px-4 w-full">
        <!-- Logo -->
        <div class="flex justify-start">
            <a href="/">
                <img src={Icon} alt="Logo" class="w-32">
            </a>
        </div>

        <!-- Links -->
        <div class="flex justify-center space-x-8">
            <!-- About Us Link -->
            <button
                class="text-lg font-medium hover:text-black hover:underline focus:outline-none"
                on:click={toggleDropdown}
            >
                About Us
            </button>
            <a href="/" class="text-lg font-medium hover:text-black hover:underline">Our Work</a>
            <a href="/" class="text-lg font-medium hover:text-black hover:underline">Ideas</a>
        </div>

        <!-- Donate -->
        <div class="flex justify-end">
            <a href="/" class="text-lg hover:text-black hover:underline">Donate</a>
        </div>
    </div>

    <!-- Dropdown -->
    {#if isDropdownOpen}
        <div class="absolute left-0 top-full w-full bg-white shadow-md p-6 font-thin">
            <div class="grid grid-cols-3 gap-6">
                <!-- Column 1 -->
                <div>
                    <h4 class=" text-2xl font-base">About Us</h4>
                    <p class="mt-2 text-sm text-gray-600">
                        Learn about our story, our operation and our role in making the world one step better at a time.
                    </p>
                </div>
                <!-- Column 2 -->
                <div>
                    <h4 class=" text-2xl font-base">Explore</h4>
                    <ul class="mt-2 space-y-2">
                        <li><a href="/about/our-story" class="text-sm text-gray-600 hover:underline" on:click={closeDropdown}>Our Story</a></li>
                        <li><a href="/" class="text-sm text-gray-600 hover:underline" on:click={closeDropdown}>FAQ</a></li>
                        <li><a href="/" class="text-sm text-gray-600 hover:underline" on:click={closeDropdown}>Our Team</a></li>
                        <li><a href="/" class="text-sm text-gray-600 hover:underline" on:click={closeDropdown}>Financials</a></li>
                        <li><a href="/" class="text-sm text-gray-600 hover:underline" on:click={closeDropdown}>Media Center</a></li>
                    </ul>
                </div>
                <!-- Column 3 -->
                <div>
                    <h4 class=" text-2xl font-base">Get Involved</h4>
                    <ul class="mt-2 space-y-2">
                        <li><a href="/" class="text-sm text-gray-600 hover:underline" on:click={closeDropdown}>How We Work</a></li>
                        <li><a href="/" class="text-sm text-gray-600 hover:underline" on:click={closeDropdown}>Volunteer</a></li>
                        <li><a href="/" class="text-sm text-gray-600 hover:underline" on:click={closeDropdown}>Ways to Give</a></li>
                        <li><a href="/" class="text-sm text-gray-600 hover:underline" on:click={closeDropdown}>Contact</a></li>
                    </ul>
                </div>
            </div>
        </div>
    {/if}
</nav>
        <div class="my-16">
          <slot/>
        </div>
          <footer class="p-8 border-t grid grid-cols-3 gap-8">
              <div>
                  <a href="/">
                      <img href="" class="items-center w-32" src={Icon} alt="Logo">
                  </a>
              </div>
              <div>
                  <p class="text-[1rem]">We are a nonprofit fighting poverty and inequity around the world.</p>
              </div>
              <div class="flex justify-end gap-8 items-center text-2xl">
                  <button aria-label="Tiktok">
                      <a href="https://www.tiktok.com/@solaceglobalnpo" target="_blank" aria-label="Tiktok">
                          <i class="fa-brands fa-tiktok"></i>
                      </a>
                  </button>
                  <button aria-label="Instagram">
                      <a href="https://www.instagram.com/solaceglobalnpo/" target="_blank" aria-label="Instagram">
                          <i class="fa-brands fa-instagram"></i>
                      </a>
                  </button>
                  <button aria-label="Youtube">
                      <a href="https://www.youtube.com/@SolaceGlobalNPO1" target="_blank" aria-label="Youtube">
                          <i class="fa-brands fa-youtube"></i>
                      </a>
                  </button>               
              </div>
        </footer>

      </div>
    <div class="flex-grow"></div>
  </div>
</main>


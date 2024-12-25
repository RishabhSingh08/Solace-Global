
<script>
import "../app.css";
import '@fortawesome/fontawesome-free/css/all.min.css';
import Icon from "../lib/images/SolaceGlobalLogo.png";

let isAboutDropdownOpen = false;
let isWorkDropdownOpen = false;
let isIdeasDropdownOpen = false;

function closeAllDropdowns() {
    isAboutDropdownOpen = false;
    isWorkDropdownOpen = false;
    isIdeasDropdownOpen = false;
}

function toggleAboutDropdown() {
    isAboutDropdownOpen = !isAboutDropdownOpen;
    isWorkDropdownOpen = false;
    isIdeasDropdownOpen = false;
}

function toggleWorkDropdown() {
    isWorkDropdownOpen = !isWorkDropdownOpen;
    isAboutDropdownOpen = false;
    isIdeasDropdownOpen = false;
}

function toggleIdeasDropdown() {
    isIdeasDropdownOpen = !isIdeasDropdownOpen;
    isAboutDropdownOpen = false;
    isWorkDropdownOpen = false;
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
            <button
                class="text-lg font-medium hover:text-black hover:underline focus:outline-none"
                on:click={toggleAboutDropdown}
            >
                About Us
            </button>
            <button
                class="text-lg font-medium hover:text-black hover:underline focus:outline-none"
                on:click={toggleWorkDropdown}
            >
                Our Work
            </button>
            <button
                class="text-lg font-medium hover:text-black hover:underline focus:outline-none"
                on:click={toggleIdeasDropdown}
            >
                Ideas
            </button>
        </div>

        <!-- Donate -->
        <div class="flex justify-end">
            <a href="/donate" class="text-lg hover:text-black hover:underline">Donate</a>
        </div>
    </div>

    <!-- Dropdowns -->
    {#if isAboutDropdownOpen}
    <div id="dropdown-about-menu" class="absolute left-0 top-full w-full bg-white shadow-md p-6 font-thin border-t">
        <div class="grid grid-cols-3 gap-6">
            <!-- Column 1 -->
            <div class="">
                <h4 class="text-2xl font-base ">About Us</h4>
                <p class="mt-2 text-lg w-96 ">Learn about our story, our operation and our role in making the world one step better at a time</p>
            </div>
            <!-- Column 2 -->
            <div>
                <h4 class="text-2xl font-base">Explore</h4>
                <ul class="mt-2 space-y-2">
                    <li><a href="/about/our-story" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>Our Story</a></li>
                    <li><a href="/about/FAQ" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>FAQ</a></li>
                    <li><a href="/about/our-team" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>Our Team</a></li>
                    <li><a href="/about/financials" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>Financials</a></li>
                </ul>
            </div>
            <!-- Column 3 -->
            <div>
                <h4 class="text-2xl font-base">Get Involved</h4>
                <ul class="mt-2 space-y-2">
                    <li><a href="/about/how-we-work" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>How We Work</a></li>
                    <li><a href="/about/volunteer" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>Volunteer</a></li>
                    <li><a href="/" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>Ways to Give</a></li>
                    <li><a href="/about/contact" class=" text-gray-600 hover:underline on:click={closeAllDropdowns}">Contact</a></li>
                </ul>
            </div>
        </div>
    </div>
{/if}

    {#if isWorkDropdownOpen}
    <div id="dropdown-menu-work" class="absolute left-0 top-full w-full bg-white shadow-md p-6 font-thin border-t">
        <div class="grid grid-cols-4 gap-6">
            <!-- Column 1 -->
            <div>
                <h4 class="text-2xl font-base">Our Work</h4>
                <p class="mt-2 text-lg ">Explore how we operate and the methods we use to create meaningful change.</p>
            </div>
                    <!-- Column 2 -->
            <div>
                <h4 class="text-2xl font-base"><a href="/work/girls-in-stem" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>Girls in STEM</a></h4>
                <ul class="mt-2 space-y-2">
                    <li><a href="/work/girls-in-stem/#tech-builders" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>Tech Builders</a></li>
                    <li><a href="/work/girls-in-stem/#CodeHER" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>CodeHER</a></li>
                </ul>
            </div>
            <div>
                <h4 class="text-2xl font-base"><a href="/work/connection-project" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>The Connection Project</a></h4>
                <ul class="mt-2 space-y-2">
                    <li><a href="/work/connection-project/#tech-builders" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>Chess for Change</a></li>
                    <li><a href="/work/connection-project/#melodies" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>Melodies for Memories</a></li>
                    <li><a href="/work/connection-project/#creations" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>3D Commemorative Creations</a></li>
                </ul>
            </div>
            <div>
                <h4 class="text-2xl font-base"><a href="/work/discovery-project" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>The Discovery Project</a></h4>
                <ul class="mt-2 space-y-2">
                    <li><a href="/work/discovery-project/#dreams" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>3D Dreams: Empowering Kids
</a></li>
                    <li><a href="/work/discovery-project/#robots" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>Robots for Earth

</a></li>
                    <li><a href="/work/discovery-project/#seniors" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>Smart Seniors
</a></li>
                    <li><a href="/work/discovery-project/#spark" class=" text-gray-600 hover:underline" on:click={closeAllDropdowns}>STEM Spark</a></li>
                    <li></li>
                </ul>
            </div>
        </div>    
    </div>
    {/if}

    {#if isIdeasDropdownOpen}
    <div id="dropdown-menu-ideas" class="absolute left-0 top-full w-full bg-white shadow-md p-6 font-thin border-t">
        <div class="grid grid-cols-3 gap-6">
            <!-- Column 1 -->
            <div>
                <h4 class="text-2xl font-base">Ideas</h4>
                <p class="mt-2 text-lg">
                    Learn about our story, our operation and our role in making the world one step better at a time.
                </p>
            </div>
            <!-- Column 2 -->
            <div>
                <h4 class="text-2xl font-base">Explore</h4>
                <ul class="mt-2 space-y-2">
                    <li><a href="/ideas/our-story" class=" text-gray-600 hover:underline">Our Story</a></li>
                    <li><a href="/ideas/FAQ" class=" text-gray-600 hover:underline">FAQ</a></li>
                    <li><a href="/ideas/our-team" class=" text-gray-600 hover:underline">Our Team</a></li>
                    <li><a href="/ideas/financials" class=" text-gray-600 hover:underline">Financials</a></li>
                </ul>
            </div>
            <!-- Column 3 -->
            <div>
                <h4 class="text-2xl font-base">Get Involved</h4>
                <ul class="mt-2 space-y-2">
                    <li><a href="/about/how-we-work" class=" text-gray-600 hover:underline">How We Work</a></li>
                    <li><a href="/about/volunteer" class=" text-gray-600 hover:underline">Volunteer</a></li>
                    <li><a href="/" class=" text-gray-600 hover:underline">Ways to Give</a></li>
                    <li><a href="/about/contact" class=" text-gray-600 hover:underline">Contact</a></li>
                </ul>
            </div>
        </div>    </div>
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
        <p class="text-sm text-center">We are a student-led nonprofit focused on empowering underserved communities through support, innovation, and impactful outreach programs.</p>
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



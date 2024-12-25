<script>
  let currentSection = 1;
  let name = "";
  let email = "";
  let selectedCategory = "";
  let selectedCauses = [];
  let donationAmount = 0;

  // Medical causes
  let medicalCauses = {
    Cancer: 0,
    Malaria: 0,
    Cardiovascular: 0,
    Respiratory: 0,
  };

  // Global conflict causes
  let globalConflicts = {
    "European Conflict": 0,
    "Asian Conflict": 0,
    "African Conflict": 0,
    "South American Conflict": 0,
    "Other War Affected Areas": 0,
  };

  // Learning causes
  let learningCauses = {
    Europe: 0,
    Asia: 0,
    "North America": 0,
    "South America": 0,
    Australia: 0,
    Africa: 0,
  };

  function nextSection() {
    // Validate name and email at the first step
    if (currentSection === 1 && (!name || !email)) {
      alert("Please enter your name and email.");
      return;
    }

    // Check for causes if on the causes selection page
    if (currentSection === 2 && selectedCategory === "Causes" && selectedCauses.length === 0) {
      currentSection = 6; // Skip to summary if no causes are selected
      return;
    }

    currentSection++;
  }

  function previousSection() {
    currentSection--;
  }

  function calculateTotal() {
    let total = donationAmount;
    return total;
  }

  function validatePercentages(causes) {
    let totalPercentage = Object.values(causes).reduce((sum, value) => sum + value, 0);
    if (totalPercentage > 100) {
      alert("The total percentage cannot exceed 100%.");
      return false;
    }
    return true;
  }

  function generateUrl() {
    let message = `Total Donation: $${donationAmount.toFixed(2)}\n\n`;

    if (selectedCategory === "Causes") {
      if (selectedCauses.includes("Medical")) {
        message += "Medical Causes\n";
        for (let cause in medicalCauses) {
          if (medicalCauses[cause] > 0) {
            message += `- ${cause}:: ${medicalCauses[cause]}% ($${(
              (medicalCauses[cause] / 100) *
              donationAmount
            ).toFixed(2)})\n`;
          }
        }
      }
      if (selectedCauses.includes("Global Learning")) {
        message += "Global Conflict Causes\n";
        for (let conflict in globalConflicts) {
          if (globalConflicts[conflict] > 0) {
            message += `- ${conflict}:: ${globalConflicts[conflict]}% ($${(
              (globalConflicts[conflict] / 100) *
              donationAmount
            ).toFixed(2)})\n`;
          }
        }
      }
      if (selectedCauses.includes("Learning Causes")) {
        message += "Learning Causes\n";
        for (let region in learningCauses) {
          if (learningCauses[region] > 0) {
            message += `- ${region}:: ${learningCauses[region]}% ($${(
              (learningCauses[region] / 100) *
              donationAmount
            ).toFixed(2)})\n`;
          }
        }
      }
    }

    const encodedMessage = encodeURIComponent(message);
    const url = `https://hcb.hackclub.com/donations/start/solace-global?name=${name}&email=${email}&message=${encodedMessage}&amount=${(
      donationAmount * 100
    ).toFixed(0)}`;
    return url;
  }
</script>

<div class="max-w-lg mx-auto p-6 bg-white shadow-md rounded-lg">
  {#if currentSection === 1}
  <div>
    <h2 class="text-xl font-bold mb-4">Enter Your Details</h2>
    <label class="block mb-2">Name</label>
    <input
      type="text"
      bind:value={name}
      class="w-full p-2 border rounded mb-4"
      placeholder="Your Name"
    />
    <label class="block mb-2">Email</label>
    <input
      type="email"
      bind:value={email}
      class="w-full p-2 border rounded mb-4"
      placeholder="Your Email"
    />
    <h3 class="text-lg font-bold mb-2">What do you want to donate to?</h3>
    <button
      class="block w-full p-2 bg-blue-500 text-white rounded mb-2"
      on:click={() => {
        selectedCategory = "Causes";
        nextSection();
      }}
    >
      Causes (War, Education, Learning)
    </button>
    <button
      class="block w-full p-2 bg-green-500 text-white rounded"
      on:click={() => {
        selectedCategory = "Robotics";
        currentSection = 6; // Skip to donation summary
      }}
    >
      Robotics Kits and Chess Boards
    </button>
  </div>
  {/if}

  {#if currentSection === 2 && selectedCategory === "Causes"}
  <div>
    <h2 class="text-xl font-bold mb-4">Select Causes</h2>
    <label class="block mb-2">
      <input type="checkbox" bind:group={selectedCauses} value="Medical" /> Medical
    </label>
    <label class="block mb-2">
      <input type="checkbox" bind:group={selectedCauses} value="Global Learning" /> Global Learning
    </label>
    <label class="block mb-2">
      <input type="checkbox" bind:group={selectedCauses} value="Learning Causes" /> Learning Causes
    </label>
    <label class="block mb-2">Donation Amount ($)</label>
    <input
      type="number"
      bind:value={donationAmount}
      class="w-full p-2 border rounded mb-4"
      placeholder="Enter donation amount"
    />
    <div class="flex justify-between">
      <button class="block w-2/5 p-2 bg-gray-500 text-white rounded" on:click={previousSection}>
        Previous
      </button>
      <button class="block w-2/5 p-2 bg-red-500 text-white rounded" on:click={nextSection}>
        Next
      </button>
    </div>
  </div>
  {/if}

  {#if currentSection === 3 && selectedCauses.includes("Medical")}
  <div>
    <h2 class="text-xl font-bold mb-4">Medical Causes</h2>
    {#each Object.keys(medicalCauses) as cause}
    <label class="block mb-2">
      {cause}:
      <input
        type="number"
        bind:value={medicalCauses[cause]}
        class="w-full p-2 border rounded mb-2"
        placeholder="Enter percentage"
      />
    </label>
    {/each}
    <div class="flex justify-between">
      <button class="block w-2/5 p-2 bg-gray-500 text-white rounded" on:click={previousSection}>
        Previous
      </button>
      <button class="block w-2/5 p-2 bg-red-500 text-white rounded" on:click={nextSection}>
        Next
      </button>
    </div>
  </div>
  {/if}

  {#if currentSection === 4 && selectedCauses.includes("Global Learning")}
  <div>
    <h2 class="text-xl font-bold mb-4">Global Conflict Causes</h2>
    {#each Object.keys(globalConflicts) as conflict}
    <label class="block mb-2">
      {conflict}:
      <input
        type="number"
        bind:value={globalConflicts[conflict]}
        class="w-full p-2 border rounded mb-2"
        placeholder="Enter percentage"
      />
    </label>
    {/each}
    <div class="flex justify-between">
      <button class="block w-2/5 p-2 bg-gray-500 text-white rounded" on:click={previousSection}>
        Previous
      </button>
      <button class="block w-2/5 p-2 bg-red-500 text-white rounded" on:click={nextSection}>
        Next
      </button>
    </div>
  </div>
  {/if}

  {#if currentSection === 5 && selectedCauses.includes("Learning Causes")}
  <div>
    <h2 class="text-xl font-bold mb-4">Learning Causes</h2>
    {#each Object.keys(learningCauses) as region}
    <label class="block mb-2">
      {region}:
      <input
        type="number"
        bind:value={learningCauses[region]}
        class="w-full p-2 border rounded mb-2"
        placeholder="Enter percentage"
      />
    </label>
    {/each}
    <div class="flex justify-between">
      <button class="block w-2/5 p-2 bg-gray-500 text-white rounded" on:click={previousSection}>
        Previous
      </button>
      <button class="block w-2/5 p-2 bg-red-500 text-white rounded" on:click={nextSection}>
        Next
      </button>
    </div>
  </div>
  {/if}

  {#if currentSection > 5}
  <div>
    <h2 class="text-xl font-bold mb-4">Summary</h2>
    <p>Total Donation: ${calculateTotal()}</p>
    {#if selectedCauses.includes("Medical")}
    <div>
      <h3 class="text-lg font-bold">Medical Causes</h3>
      {#each Object.keys(medicalCauses) as cause}
      {#if medicalCauses[cause] > 0}
      <p>- {cause}:: {medicalCauses[cause]}% (${((medicalCauses[cause] / 100) * donationAmount).toFixed(2)})</p>
      {/if}
      {/each}
    </div>
    {/if}
    {#if selectedCauses.includes("Global Learning")}
    <div>
      <h3 class="text-lg font-bold">Global Conflict Causes</h3>
      {#each Object.keys(globalConflicts) as conflict}
      {#if globalConflicts[conflict] > 0}
      <p>- {conflict}:: {globalConflicts[conflict]}% (${((globalConflicts[conflict] / 100) * donationAmount).toFixed(2)})</p>
      {/if}
      {/each}
    </div>
    {/if}
    {#if selectedCauses.includes("Learning Causes")}
    <div>
      <h3 class="text-lg font-bold">Learning Causes</h3>
      {#each Object.keys(learningCauses) as region}
      {#if learningCauses[region] > 0}
      <p>- {region}:: {learningCauses[region]}% (${((learningCauses[region] / 100) * donationAmount).toFixed(2)})</p>
      {/if}
      {/each}
    </div>
    {/if}
    <a href={generateUrl()} class="block mt-4 p-2 bg-red-500 text-center text-white rounded">
      Donate Now
    </a>
    <button class="block w-full p-2 bg-gray-500 text-white rounded mt-2" on:click={previousSection}>
      Previous
    </button>
  </div>
  {/if}
</div>

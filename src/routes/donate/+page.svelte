<script>
  import Logo from "../../lib/images/favicon.png";

  let name = "";
  let email = "";
  let amount = "";
  let message = "";
  let donationType = "Solace Global";

  let nameError = false;
  let emailError = false;
  let amountError = false;
  let formError = false;

  // Function to create the donation link
  function generateLink() {
    nameError = !name;
    emailError = !email;
    amountError = !amount;
    formError = nameError || emailError || amountError;

    if (formError) {
      return;
    }

    const formattedAmount = (parseFloat(amount) * 100).toFixed(0); // Convert to cents
    const encodedName = encodeURIComponent(name);
    const encodedEmail = encodeURIComponent(email);
    const encodedMessage = encodeURIComponent(
      `Total Donation: $${amount}\n\n${message}\n\nDonation Type: ${donationType}`
    );

    return `https://hcb.hackclub.com/donations/start/solace-global?name=${encodedName}&email=${encodedEmail}&message=${encodedMessage}&amount=${formattedAmount}`;
  }
</script>


<style>
</style>

<main>
  <div class="flex items-center justify-center bg-white min-h-screen">
    <div class="w-full max-w-lg border p-6 rounded-lg shadow-2xl">
      <h2 class="text-3xl font-semibold text-black text-center my-4 ">Make a Donation</h2>
      <img src={Logo} alt="Solace Global Logo" class="mb-6 mx-auto">
      <p class="text-center text-gray-600 mb-6 ">
        Your generous contributions help us make a global impact. Choose a cause and join us in building a brighter future.
      </p>
  
      <form
        on:submit|preventDefault={() => {
          const link = generateLink();
          if (link) {
            window.location.href = link;
          }
        }}
        class="space-y-6"
      >
        <div>
          <p class="block text-sm font-medium text-gray-700">Name*</p>
          <input
            type="text"
            bind:value={name}
            placeholder="Your Name"
            
            class={`w-full px-4 py-2 mt-1 border rounded-lg focus:ring focus:ring-red-500 outline-none ${
              nameError ? "border-red-500" : ""
            }`}
          />
        </div>
  
        <div>
          <p class="block text-sm font-medium text-gray-700">Email*</p>
          <input
            type="email"
            bind:value={email}
            placeholder="Your Email"
            
            class={`w-full px-4 py-2 mt-1 border rounded-lg focus:ring focus:ring-red-500 outline-none ${
              emailError ? "border-red-500" : ""
            }`}
          />
        </div>
  
        <div>
          <p class="block text-sm font-medium text-gray-700">Amount (USD)*</p>
          <input
            type="number"
            bind:value={amount}
            placeholder="Enter Amount"
            min="1"
            
            class={`w-full px-4 py-2 mt-1 border rounded-lg focus:ring focus:ring-red-500 outline-none ${
              amountError ? "border-red-500" : ""
            }`}
          />
        </div>
  
        <div>
          <p class="block text-sm font-medium text-gray-700">Cause you want to donate towards*</p>
          <select
            bind:value={donationType}
            class="w-full px-4 py-2 mt-1 border rounded-lg focus:ring focus:ring-red-500 outline-none"
          >
            <option value="Solace Global">General / Solace Global</option>
            <option value="Medical">Medical</option>
            <option value="Global Conflict">Global Conflict</option>
            <option value="Global Education">Global Education</option>
          </select>
        </div>
  
        <div>
          <p class="block text-sm font-medium text-gray-700">Message</p>
          <textarea
            bind:value={message}
            placeholder="Write a message (optional)"
            class="w-full px-4 py-2 mt-1 border rounded-lg focus:ring focus:ring-red-500 focus:border-red-500"
          ></textarea>
        </div>
  
        {#if formError}
          <p class="mt-4 text-center text-red-500 font-semibold">
            Incomplete Fields
          </p>
        {/if}
        <button
          type="submit"
          class="w-full px-4 py-2 text-white bg-red-500 rounded-lg hover:bg-red-600 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500"
        >
          Donate Now
        </button>
  
      </form>
    </div>
  </div>
</main>

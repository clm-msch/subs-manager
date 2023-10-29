<script lang="ts">
    import ShowSub from "./ShowSub.svelte";

    let price = "";
    let withdrawalDate = ""
    let service = "";
    let customService = "";
    let subs: any[] = [];

    const services = ["Netflix", "Prime Video", "Disney+", "Spotify", "Deezer", "Xbox Game Pass", "ChatGPT", "Autre"];

    let errorMessage = "";

    function handleAddSub() {
      if (!price || !withdrawalDate.trim() || (service === "Autre" && !customService.trim())) {
        errorMessage = "N'oublie pas de remplir tous les champs !";
        return;
      }

      let finalService = service === "Autre" ? customService : service;
  
      subs = [...subs, { id: new Date().getTime(), price, withdrawalDate, service: finalService }];
      price = withdrawalDate = customService = "";
      service = "";
      errorMessage = "";
    }

    function deleteSubs(id: number) {
      subs = subs.filter(subs => subs.id !== id);
    }
  </script>
  
  <form on:submit|preventDefault={handleAddSub} class="mx-auto bg-white rounded-xl shadow-md overflow-hidden p-6">
    <h2 class="text-xl font-medium text-black mb-4">Ajouter un abonnement</h2>

    <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="price">Prix de l'abo:</label>
        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="price" type="number" bind:value={price} placeholder="0" />
    </div>

    <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="withdrawalDate">Date de prélèvement:</label>
        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="withdrawalDate" type="date" bind:value={withdrawalDate} />
    </div>

    <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="service">Service d'abonnement:</label>
        <select class="shadow border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="service" bind:value={service}>
            {#each services as serviceOption}
            <option value={serviceOption}>{serviceOption}</option>
            {/each}
        </select>
    </div>

    {#if service === 'Autre'}
    <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="customService">Service personnalisé:</label>
        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="customService" type="text" bind:value={customService} placeholder="Entrez le nom du service" />
    </div>
    {/if}

    <div class="flex items-center justify-between">
        <button class="bg-gray-800 px-4 py-3 w-full justify-center flex rounded-lg text-white text-center" type="submit">
            Ajouter
        </button>
    </div>
    {#if errorMessage}
    <p class="text-red-500">{errorMessage}</p>
    {/if}
</form>

  <ShowSub subs={subs} onDelete={deleteSubs} />

  
  

  
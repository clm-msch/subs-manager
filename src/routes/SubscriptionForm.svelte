<script lang="ts">
let price = "";
let withdrawalDate = "";
let service = "";
let customService = "";

function handleSubmit() {
    if (service === 'Autre' && customService === '') {
        alert("Veuillez remplir le champ du service personnalisé.");
        return;
    }
    console.log({
        price,
        withdrawalDate,
        service,
        customService
    });
}
</script>

<div class="mx-auto bg-white rounded-xl shadow-md overflow-hidden p-6">
    <h2 class="text-xl font-medium text-black mb-4">Ajouter un abonnement</h2>

    <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="price">Prix de l'abo:</label>
        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="price" type="number" bind:value={price} placeholder="0.00€" />
    </div>

    <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="withdrawalDate">Date de prélèvement:</label>
        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="withdrawalDate" type="date" bind:value={withdrawalDate} />
    </div>

    <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="service">Service d'abonnement:</label>
        <select class="shadow border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="service" bind:value={service}>
            <option>Netflix</option>
            <option>Prime Video</option>
            <option>Disney+</option>
            <option>Spotify</option>
            <option>Deezer</option>
            <option>Xbox Game Pass</option>
            <option>ChatGPT</option>
            <option>Autre</option>
        </select>
    </div>

    {#if service === 'Autre'}
    <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="customService">Service personnalisé:</label>
        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="customService" type="text" bind:value={customService} placeholder="Entrez le nom du service" />
    </div>
    {/if}

    <div class="flex items-center justify-between">
        <button class="bg-gray-800 px-4 py-3 w-full justify-center flex rounded-lg text-white text-center" type="button" on:click={handleSubmit}>
            Ajouter
        </button>
    </div>
</div>

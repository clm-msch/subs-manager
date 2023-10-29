<script lang="ts">
    export let subs: any[];
    export let onDelete: (id: number) => void;
  
    function handleDelete(id: number) {
      onDelete(id);
    }
  </script>
   {#each subs as sub, i (i)}
    <div class="mx-auto bg-white rounded-xl shadow-md sm:flex flex-row">
        <div class="p-6">
            <div class="flex items-center">
                <h1 class="text-xl font-medium text-black mr-2">{sub.service}</h1>
                <p class="text-sm italic">{sub.withdrawalDate}</p>
            </div>
            <div class="mt-2 text-gray-500">Prix : {sub.price} €</div>
            <div class="mt-4">
                <div class="bg-gray-800 px-4 py-3 w-full justify-center flex rounded-lg text-white text-center">
                    <button on:click={() => handleDelete(sub.id)}>Annuler l'abonnement</button>
                </div>
            </div>
        </div>
    </div>
    {/each}
    
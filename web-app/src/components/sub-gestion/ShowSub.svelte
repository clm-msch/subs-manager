<script lang="ts">
    export let subs: any[];
    export let onDelete: (id: number) => void;

    function handleDelete(id: number) {
        onDelete(id);
    }
</script>
{#each subs as sub, i (i)}
<div class="mx-auto border-b border-black last:border-b-0">
    <div class="p-6 flex justify-between items-center gap-2">
        <div>
            <h1 class="text-xl font-medium text-black">{sub.service}</h1>
            <div class="flex gap-2 items-center">
                <p class="text-sm italic">{sub.withdrawalDate} -</p>
                <div class="text-gray-500"><b>{sub.price} €</b>/m</div>
            </div>
        </div>
        <div class="flex gap-2">
            <div class="bg-gray-800 px-4 py-3 w-auto justify-center flex rounded-lg text-white text-center">
                <button on:click={() => handleDelete(sub.id)}>Annuler</button>
            </div>
            <div class="bg-gray-800 px-4 py-3 w-auto justify-center flex rounded-lg text-white text-center">
                <button>Modifier</button>
            </div>
        </div>
    </div>
</div> 
{/each}

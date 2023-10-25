<script lang="ts">
export let title = "";
export let date = "";
export let description = "";
export let url = "";
export let img = "";
</script>

<div class="mx-auto bg-white rounded-xl shadow-md sm:flex overflow-hidden max-w-2xl flex-row">
    <img class="object-cover sm:w-56 " src="{img}" alt="{title}">

    <div class="p-6">
        <div class="flex items-center">
            <h1 class="text-xl font-medium text-black mr-2">{title}</h1>
            <p class="text-sm italic">{date}</p>
        </div>

        <div class="mt-2 text-gray-500">{description}</div>
        <div class="mt-4">
            <div class="bg-gray-800 px-4 py-3 w-full justify-center flex rounded-lg text-white text-center">
                <a href="{url}">Annuler l'abonnement</a>
            </div>
        </div>
    </div>
</div>

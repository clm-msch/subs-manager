<script lang="ts">
    export let subscription = {
        title: "",
        date: "",
        description: "",
        url: "",
        img: ""
    };
</script>

<div class="mx-auto bg-white rounded-xl shadow-md sm:flex flex-row">
    <img class="object-cover sm:w-56 sm:rounded-l-xl" src="{subscription.img}" alt="{subscription.title}">
    <div class="p-6">
        <div class="flex items-center">
            <h1 class="text-xl font-medium text-black mr-2">{subscription.title}</h1>
            <p class="text-sm italic">{subscription.date}</p>
        </div>

        <div class="mt-2 text-gray-500">{subscription.description}</div>
        <div class="mt-4">
            <div class="bg-gray-800 px-4 py-3 w-full justify-center flex rounded-lg text-white text-center">
                <a href="{subscription.url}">Annuler l'abonnement</a>
            </div>
        </div>
    </div>
</div>

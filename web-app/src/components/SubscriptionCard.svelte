<script lang="ts">
    export let subscription = {
        service: "Service par défaut",
        withdrawalDate: "Date par défaut",
        price: "0.00€"
    };
    </script>
    
    <div class="mx-auto bg-white rounded-xl shadow-md sm:flex flex-row">
        <div class="p-6">
            <div class="flex items-center">
                <h1 class="text-xl font-medium text-black mr-2">{subscription.service}</h1>
                <p class="text-sm italic">{subscription.withdrawalDate}</p>
            </div>
            <div class="mt-2 text-gray-500">Prix : {subscription.price}</div>
            <div class="mt-4">
                <div class="bg-gray-800 px-4 py-3 w-full justify-center flex rounded-lg text-white text-center">
                    <a href="#">Annuler l'abonnement</a>
                </div>
            </div>
        </div>
    </div>
    
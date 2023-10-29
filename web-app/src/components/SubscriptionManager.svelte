<script lang="ts">
    import SubscriptionCard from './SubscriptionCard.svelte';
    import SubscriptionForm from './SubscriptionForm.svelte';
    let subscriptions: any = [];
    
    function handleNewSubscription(subscription : any) {
        subscriptions = [subscription, ...subscriptions];
    }
</script>
    <div class="md:flex gap-4 grid">
        <div>
            <SubscriptionForm on:subscriptionAdded={handleNewSubscription} />
        </div>
        <div class="grid grid-cols-2 gap-4">
                {#each subscriptions as subscription}
                <SubscriptionCard subscription={subscription} />
            {/each}
        </div>
    </div>
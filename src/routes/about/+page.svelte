<script lang="ts">
import SubscriptionCard from '../../components/SubscriptionCard.svelte';
import SubcriptionManager from '../../components/SubcriptionManager.svelte';
let default_img = 'https://placehold.co/400';
</script>
<svelte:head>
    <title>Compents Testing</title>
    <meta name="description" content="About this app" />
</svelte:head>

<div>
  <!-- <h1 class="text-3xl font-bold text-white mb-8">Components Testing</h1> -->
      <SubcriptionManager />

      <!-- <SubscriptionCard subscription={{ title: 'Netflix', date: '2023-11-15', description: 'Abonnement mensuel', url: '#', img: 'src/lib/images/netflix_default.jpg' }} /> -->

</div>

<script>
import ArticleCard from '../AboutCard.svelte';
import SubscriptionForm from '../SubscriptionForm.svelte';
import netflix from '$lib/images/netflix_default.jpg';
let default_img = 'https://placehold.co/400';
</script>
<svelte:head>
    <title>Compents Testing</title>
    <meta name="description" content="About this app" />
</svelte:head>

<div>
  <h1 class="text-3xl font-bold text-white mb-8">Components Testing</h1>
  <div class="md:flex gap-4 grid">
    <div>
    <SubscriptionForm />
  </div>
      <div class="flex flex-col gap-4">
        <ArticleCard
          title="Netflix"
          date="10 Septembre - (mensuel)"
          description="Lorem ipseum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
          url="https://www.google.com"
          img="{netflix}"
          />
          <ArticleCard
          title="Netflix"
          date="10 Septembre - (mensuel)"
          description="Lorem ipseum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
          url="https://www.google.com"
          img="{default_img}"
          />
          <ArticleCard
          title="Netflix"
          date="10 Septembre - (mensuel)"
          description="Lorem ipseum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
          url="https://www.google.com"
          img="{default_img}"
          />
    </div>
  </div>
</div>

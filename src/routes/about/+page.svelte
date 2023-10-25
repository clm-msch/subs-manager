<script>
	import ArticleCard from '../AboutCard.svelte';
  import netflix from '$lib/images/netflix_default.jpg';
  let default_img = 'https://placehold.co/400';
</script>
<svelte:head>
	<title>Compents Testing</title>
	<meta name="description" content="About this app" />
</svelte:head>


<ArticleCard 
  title="Netflix" 
  date="10 Septembre - (mensuel)" 
  description="Lorem ipseum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
  url="https://www.google.com"
  img="{netflix}"
/>

<ArticleCard 
  title="Lorem Ipseum 2" 
  date="00 - ()" 
  description="Lorem ipseum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
  url="https://www.google.com"
  img="{default_img}"
/>

<ArticleCard 
  title="Lorem Ipseum 3" 
  date="00 - ()"
  description="Lorem ipseum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
  url="https://www.google.com"
  img="{default_img}"
/>


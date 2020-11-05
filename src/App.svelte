<script>
	import Header from './LayoutComponents/Header.svelte';
</script>

<main>
	<Header/>
	<!-- <img class="blobImg" src="/images/homepagename.svg" alt="name"> -->
</main>

<style>
	main {
		height: 100%;
		position: relative;
        background-image: url("/images/Home.svg");
        background-size:100% 100%;
		background-repeat: no-repeat;
	}

	.blobImg{
		display: block;
		margin: auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
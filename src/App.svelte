<script>
	
</script>

<main>
	<h1><span class="h1Thin">Under</span>    Construction</h1>
	<div class="homeImageWrapper">
	</div>
</main>

<style>
	main {

	}
	
	h1{
		z-index: 1;
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		font-family: Condor;
		color: white;
		font-size: 40pt;
	}
	.h1Thin{
		font-weight: lighter;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}

	.homeImageWrapper{
		z-index:-1;
		width: auto;
        height: 640px;
        max-height: 100%;
        margin: 0;
        padding: 0;
        background-image: url("/images/portfolio-face-01.svg");
        background-size:100% 100%;
        background-repeat: no-repeat;
	}
</style>
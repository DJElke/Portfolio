<script>
	import {navOptions} from './Navigation/Navigation.svelte';
	let selected = navOptions[0];
	let intSelected = 0;
	let isIndex;

	const changeComponent = (event) => {
		selected = navOptions[event.srcElement.id];
		intSelected = event.srcElement.id;
	}
</script>

<main class={intSelected == 0 ? "indexMain" : ""}>
<!-- APP NAVIGATION -->
<header>
	<nav>
		<ul class="navigation">
			{#each navOptions as option, i}
				{#if i == 0}
					<li class="navigationObj navigationObj--index"><a on:click={changeComponent} id={i}>{option.page}</a></li>
				{:else}
					<li class="navigationObj"><a on:click={changeComponent} id={i}>{option.page}</a></li>
				{/if}
			{/each}
		</ul>
	</nav>
</header>

<!-- CONTENT -->
<svelte:component this={selected.component}/>
</main>


<style>
	.indexMain {
		height: 100%;
		position: relative;
        background-image: url("/images/Home.svg");
        background-size:100% 100%;
		background-repeat: no-repeat;
	}

	.navigation{
        list-style-type: none;
        margin: 0;
        padding: 0;
        height: 5rem;
        overflow: hidden;
        font-family: Condor;
        text-align: center;
        vertical-align: middle;
        line-height: 5rem;
    }

    .navigationObj{
        float: right;
        vertical-align: middle;
    }

    .navigationObj a{
        display: block;
        text-align: center;
        padding-left: 5rem;
        padding-right: 5rem;
        text-decoration: none;
		color: #EC5F33;
		cursor: pointer;
    }

    .navigationObj--index{
        float: left;
        font-size: 36px;
    }

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
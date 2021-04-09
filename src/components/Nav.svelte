<script>
	import Pictobeud from '../../static/pictobeud.png'

	let menu = [
		{ id: 1, name: 'about'},
		{ id: 2, name: 'experience'},
		{ id: 3, name: 'skills' },
		{ id: 4, name: 'interests'},
		{ id: 5, name: 'contact'}
	]

	let current= true;

	function toggle() {
		current = !current;
	}
</script>

<style type='text/scss'>
	@import "../styles/theme.scss";


	// Small Size
	
	nav {
		background-color: $main-color;
	} 

	// Medium Size

	@media (min-width: 480px) {

		}

	// Large Size

	@media (min-width: 959px) {

			nav {
		width: 250px;
		height: 100VH;
		max-height: 1000px;
		position: fixed;
		z-index: 9999;
		}

		

		.bloc-list {
			height: 70%;
			margin-top: 6rem;
			display: flex;
			flex-direction: column;
			justify-content: space-evenly;
			align-items: center;

			&--item1 {
				width: 50%;
			}

			&--item a{
				text-transform: uppercase;
				font-family: $dosis;
				font-weight: $title-bold;
				font-size: 1.5rem;
				color: $white;
			}

			&--selected a {
				text-transform: uppercase;
				font-family:$dosis;
				font-weight: $title-bold;
				font-size: 1.5rem;
				color: $black;
			}
			
			&--item:hover a {
				color: $grey;
			}
			&--picto {
		width: 80%;
		border-radius: 50%;
		border: solid 10px #cc6637;
		box-shadow: 3px 3px 2px rgba(0,0,0,0.75);
		} 

		}
	
		}

	// X-large Size
	
	@media (min-width: 1280px) {

	
		}
</style>

<nav class="bloc">
	<ul class="bloc-list">
		<li class="bloc-list--item1"><a href="."><img class="bloc-list--picto" src={Pictobeud} alt="benoit robin"></a></li>
		{#each menu as item}
		<li class="{current ? 'bloc-list--item' : 'bloc-list--selected'}"><a href={item.name} on:click={toggle}>{item.name}</a></li>
		{/each}
	</ul>
</nav>
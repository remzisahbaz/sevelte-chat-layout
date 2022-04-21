<!--main skeletal structure -->
<!--layout-->

<!--script-->
<script>
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>

<!--header-->
<Header  message=""/>

<!--body-->
<main>
	<slot />
</main>

<!--footer-->
<footer>

</footer>

<!--styles-->
<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
		color: #ff3e00;
		font-size-adjust: revert;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 150px ;

		}
	}
</style>

<!--script-->
<script context="module">
export async function load({fetch})
{
	// eslint-disable-next-line no-unused-vars
	const res= await fetch('https://jsonplaceholder.typicode.com/posts');
	// eslint-disable-next-line no-unused-vars
	const guides=await res.json();

	if(res.ok){
		return {
			props:{
				guides
			}
		}
	}
	return {
		status:res.status,
		error:new Error('Could not fetch the guides')
	};
}

</script>

<script>
	export  let guides

</script>
<!-- web site head-->
<svelte:head>
	<title>Project</title>
</svelte:head>

<!--body-->
<body class="content">
	<h1>Project this app</h1>

	<div>
		<ul>
			{#each guides as guide}
				<li>
					<a href="/">{guide.title}</a>
				</li>

				{/each}
		</ul>
	</div>
</body>



<!--style-->
<style>
	.content {
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
</style>

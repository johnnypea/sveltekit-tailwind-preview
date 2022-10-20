<script lang="ts">
	let showhide = false;
	$: sha = showhide ? 'grow' : 'grow-0';
</script>

<div class="flex flex-col h-screen">
	<div class="">
		<button
			class="px-4 py-2 font-semibold text-sm bg-sky-500 text-white rounded-none shadow-sm"
			on:click={() => (showhide = !showhide)}>
			Show/Hide
		</button>
	</div>

	<div class="flex grow flex-row items-stretch">
		<div class="flex-1 grow bg-green-600 p-5">a</div>
		<div class="flex-1 grow bg-red-600 p-5">b</div>
		<div class="{sha} bg-blue-600 transition-all duration-1000">
			{#if showhide}
				<div class="p-5">c</div>
			{/if}
		</div>
	</div>
</div>

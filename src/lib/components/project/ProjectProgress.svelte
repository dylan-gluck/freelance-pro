<script>
	import ProjectBurndown from './ProjectBurndown.svelte';
</script>

<details class="collapse collapse-arrow rounded-none">
	<summary class="collapse-title border-b border-base-300 mb-4">
		<div class="flex items-baseline gap-3">
			<h3 class="text-lg font-semibold">Burndown</h3>
		</div>
	</summary>
	<div class="collapse-content">
		<div class="flex flex-col gap-4">
			<ProjectBurndown />
		</div>
	</div>
</details>

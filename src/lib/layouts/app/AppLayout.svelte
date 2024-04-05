<script>
	import AppHeader from '$lib/layouts/app/AppHeader.svelte';
	import AppSidebar from '$lib/layouts/app/AppSidebar.svelte';
	import 'iconify-icon';
</script>

<div class="drawer lg:drawer-open">
	<input id="app-drawer" type="checkbox" class="drawer-toggle" />
	<div class="drawer-content flex flex-col items-start justify-start px-4 gap-4">
		<AppHeader />
		<!-- Page content here -->
		<slot />
	</div>
	<div class="drawer-side">
		<label for="app-drawer" aria-label="close sidebar" class="drawer-overlay"></label>
		<AppSidebar />
	</div>
</div>

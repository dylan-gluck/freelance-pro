<script>
	import AppLayout from '$lib/layouts/app/AppLayout.svelte';
	import ProjectHeader from '$lib/components/project/ProjectHeader.svelte';
	import ProjectSidebar from '$lib/components/project/ProjectSidebar.svelte';
	import ProjectPlan from '$lib/components/project/ProjectPlan.svelte';
	import ProjectProgress from '$lib/components/project/ProjectProgress.svelte';
</script>

<svelte:head>
	<title>MVP Build + AI Agent Integration | Freelance Pro</title>
</svelte:head>

<AppLayout>
	<div class="grid grid-cols-4 w-full gap-6">
		<section class="col-span-3 flex flex-col gap-4 mb-10">
			<ProjectHeader />
			<ProjectPlan />
			<ProjectProgress />
		</section>

		<ProjectSidebar />
	</div>
</AppLayout>

<script>
	import AppLayout from '$lib/layouts/app/AppLayout.svelte';
	import 'iconify-icon';
	import { onMount } from 'svelte';

	onMount(async () => {
		const { default: ApexCharts } = await import('apexcharts');

		var options = {
			series: [
				{
					name: 'Expected',
					data: [10, 9, 8, 7, 6, 4, 2, 0]
				},
				{
					name: 'Actuals',
					data: [10, 9, 6, 5, 4, 2, 2, 0]
				}
			],
			chart: {
				height: 300,
				type: 'area',
				offsetX: -15,
				toolbar: {
					show: false
				}
			},
			dataLabels: {
				enabled: false
			},
			stroke: {
				curve: 'smooth'
			},
			xaxis: {
				type: 'datetime',
				categories: [
					'2023-06-20T00:00:00.000Z',
					'2023-07-20T01:30:00.000Z',
					'2023-08-20T02:30:00.000Z',
					'2023-09-20T03:30:00.000Z',
					'2023-10-20T04:30:00.000Z',
					'2023-11-20T05:30:00.000Z',
					'2023-12-20T06:30:00.000Z'
				]
			},
			tooltip: {
				x: {
					format: 'dd/MM/yy HH:mm'
				}
			}
		};

		var chart = new ApexCharts(document.querySelector('#chart'), options);

		chart.render();
	});
</script>

<svelte:head>
	<title>Project Title | Freelance Pro</title>
</svelte:head>

<AppLayout>
	<div class="grid grid-cols-4 w-full gap-6">
		<section class="col-span-3 flex flex-col gap-4">
			<div
				class="rounded-lg bg-base-100 text-base-content p-6 w-full gap-4 grid grid-cols-1 lg:grid-cols-3"
			>
				<div class="flex flex-col col-span-2">
					<h1 class="text-3xl lg:text-5xl max-w-3xl pb-4">VisionDeck MVP</h1>
					<h3 class="text-lg lg:text-xl text-primary">Full-stack App Build</h3>
				</div>
				<div class="flex flex-col gap-3">
					<div class="flex justify-between items-center w-full gap-6">
						<span class="stat-title">Project status</span>
						<span class="badge badge-md badge-neutral gap-1"
							><span class="badge-xs badge badge-info"></span> On track</span
						>
					</div>
					<div class="flex justify-between items-center w-full gap-6">
						<span class="stat-title">Checkpoint</span>
						<span>April 20, 2024</span>
					</div>
					<div class="flex justify-between items-center w-full gap-6">
						<span class="stat-title">Progress</span>
						<progress class="progress progress-primary" value="90" max="100"></progress>
					</div>
				</div>
			</div>

			<!-- <div class="stats shadow flex w-full bg-base-200">
				<div class="stat gap-2">
					<div class="stat-figure text-neutral">
						<iconify-icon icon="bi:pin-map" class="text-4xl"></iconify-icon>
					</div>
					<div class="stat-title">Checkpoint</div>
					<div class="stat-value">1 / 2</div>
					<div class="stat-desc">
						<span class="badge badge-md badge-neutral gap-1"
							><span class="badge-xs badge badge-success"></span> On schedule</span
						>
					</div>
				</div>
				<div class="stat gap-2">
					<div class="stat-figure text-neutral">
						<iconify-icon icon="material-symbols:fact-check-outline" class="text-4xl"
						></iconify-icon>
					</div>
					<div class="stat-title">Tasks</div>
					<div class="stat-value">10 / 12</div>
					<div class="stat-desc">
						<progress class="progress w-full progress-primary" value="80" max="100"></progress>
					</div>
				</div>
				<div class="stat gap-2">
					<div class="stat-figure text-neutral">
						<iconify-icon icon="solar:money-bag-bold" class="text-4xl"></iconify-icon>
					</div>
					<div class="stat-title">Due</div>
					<div class="stat-value">$15,000</div>
					<div class="stat-desc">
						<span class="badge badge-md badge-neutral gap-1"
							><span class="badge-xs badge badge-warning"></span> Pending</span
						>
					</div>
				</div>
			</div> -->

			<div class="rounded-lg bg-base-200 text-base-content w-full">
				<div class="grid grid-cols-1 gap-px sm:grid-cols-2 lg:grid-cols-4">
					<div class="px-4 py-6 sm:px-6 lg:px-8">
						<p class="text-sm font-medium leading-6 text-gray-400">Checkpoint</p>
						<p class="mt-2 flex items-baseline gap-x-2">
							<span class="text-4xl font-semibold tracking-tight">2 / 2</span>
							<span class="badge badge-sm badge-neutral">Aug 20, 2022</span>
						</p>
					</div>
					<div class="px-4 py-6 sm:px-6 lg:px-8">
						<p class="text-sm font-medium leading-6 text-gray-400">Progress</p>
						<p class="mt-2 flex items-baseline gap-x-2">
							<span class="text-4xl font-semibold tracking-tight">90%</span>
							<span class="badge badge-sm badge-neutral">On track</span>
						</p>
					</div>
					<div class="px-4 py-6 sm:px-6 lg:px-8">
						<p class="text-sm font-medium leading-6 text-gray-400">Tasks</p>
						<p class="mt-2 flex items-baseline gap-x-2">
							<span class="text-4xl font-semibold tracking-tight">9 / 10</span>
						</p>
					</div>
					<div class="px-4 py-6 sm:px-6 lg:px-8">
						<p class="text-sm font-medium leading-6 text-gray-400">Due on delivery</p>
						<p class="mt-2 flex items-baseline gap-x-2">
							<span class="text-4xl font-semibold tracking-tight">$15,000</span>
							<span class="badge badge-sm badge-neutral">Pending</span>
						</p>
					</div>
				</div>
			</div>

			<div class="grid grid-cols-1">
				<div class="rounded-lg bg-base-300 text-base-content p-6 w-full">
					<h3 class="text-md font-semibold">Burndown</h3>
					<div id="chart"></div>
				</div>
			</div>
		</section>
		<aside>
			<div class="rounded-lg bg-base-100 text-base-content flex flex-col gap-4 p-4 w-full">
				<div class="flex flex-col gap-2">
					<h4 class="text-md font-semibold">Client</h4>
					<ul class="menu p-0">
						<li>
							<a href="/clients/visiondeck">
								<img
									src="https://visiondeck.io/images/mark.png"
									alt="visiondeck mark"
									class="w-8"
								/>
								<span class="text-2xl">VisionDeck</span>
							</a>
						</li>
					</ul>
				</div>
				<div class="flex flex-col gap-2">
					<div class="flex justify-between items-center">
						<h4 class="text-md font-semibold">Contacts</h4>
						<button type="button" class="btn btn-xs btn-square btn-ghost">
							<iconify-icon icon="ph:plus"></iconify-icon>
						</button>
					</div>
					<ul class="menu p-0">
						<li>
							<a href="/user/drew@visiondeck.io">
								<div class="avatar online">
									<div class="w-8 rounded-full">
										<img
											src="https://daisyui.com/images/stock/photo-1534528741775-53994a69daeb.jpg"
											alt="avatar"
										/>
									</div>
								</div>
								<span>drew@visiondeck.io</span>
							</a>
						</li>
						<li>
							<a href="/user/jmp@visiondeck.io">
								<div class="avatar online placeholder">
									<div class="bg-neutral text-neutral-content rounded-full w-8">
										<span class="text-xl">JP</span>
									</div>
								</div>
								<span>jmp@visiondeck.io</span>
							</a>
						</li>
					</ul>
				</div>
				<div class="flex flex-col gap-2">
					<div class="flex justify-between items-center">
						<h4 class="text-md font-semibold">Bookmarks</h4>
						<button type="button" class="btn btn-xs btn-square btn-ghost">
							<iconify-icon icon="ph:plus"></iconify-icon>
						</button>
					</div>
					<ul class="menu p-0">
						<li>
							<!-- svelte-ignore a11y-invalid-attribute -->
							<a href="#">
								<iconify-icon icon="solar:link-bold"></iconify-icon>
								<span>Brand style guide</span>
							</a>
						</li>
						<li>
							<!-- svelte-ignore a11y-invalid-attribute -->
							<a href="#">
								<iconify-icon icon="solar:link-bold"></iconify-icon>
								<span>Designs</span>
							</a>
						</li>
					</ul>
				</div>
				<!-- <div class="flex flex-col gap-3">
					<h4 class="text-md font-semibold">Actions</h4>
					<button type="button" class="btn">Generate Invoice & Send</button>
				</div> -->
			</div>
		</aside>
	</div>
</AppLayout>

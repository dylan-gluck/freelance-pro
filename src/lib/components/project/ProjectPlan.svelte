<script>
	import ProjectTimeline from './ProjectTimeline.svelte';
</script>

<details class="collapse collapse-arrow rounded-none">
	<summary class="collapse-title border-b border-base-300 mb-4">
		<div class="flex items-baseline gap-3">
			<h3 class="text-lg font-semibold">Project Plan</h3>
			<span class="badge badge-sm badge-primary">Approved</span>
		</div>
	</summary>
	<div class="collapse-content">
		<div class="grid grid-cols-3 gap-2">
			<div class="flex flex-col gap-8 overflow-x-auto col-span-2">
				<div>
					<h4 class="text-md font-semibold mb-2">Overview</h4>
					<p>
						Nulla vitae elit libero, a pharetra augue. Aenean eu leo quam. Pellentesque ornare sem
						lacinia quam venenatis vestibulum. Lorem ipsum dolor sit amet, consectetur adipiscing
						elit. Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor.
					</p>
				</div>
				<div>
					<table class="table table-sm bg-base-300 text-base-content overflow-clip rounded-md">
						<tbody>
							<tr>
								<td class="font-bold">Structure</td>
								<td>Fixed Bid</td>
							</tr>
							<tr>
								<td class="font-bold">Payments</td>
								<td>Monthly</td>
							</tr>
							<tr>
								<td class="font-bold">Project Cost</td>
								<td>$40,000</td>
							</tr>
							<tr>
								<td class="font-bold">Deposit</td>
								<td>$3,000</td>
							</tr>
							<tr class="bg-neutral text-neutral-content">
								<td class="font-bold">Collected To-Date</td>
								<td>$20,000</td>
							</tr>
						</tbody>
					</table>
				</div>
				<div>
					<h4 class="text-md font-semibold mb-4">Documents</h4>
					<ul class="menu menu-md bg-base-200 rounded-md">
						<li>
							<button>
								<span>Project Terms</span>
								<span class="badge badge-sm">2</span>
								<span class="badge badge-sm">Signed</span>
							</button>
						</li>
						<li>
							<button>
								<span>Invoices</span>
								<span class="badge badge-sm">10</span>
								<span class="badge badge-sm badge-secondary">1 Outstanding</span>
							</button>
						</li>
						<li>
							<button>
								<span>Change Orders</span>
								<span class="badge badge-sm">2</span>
								<span class="badge badge-sm">Signed</span>
							</button>
						</li>
					</ul>
				</div>
				<div class="flex items-center gap-2">
					<button class="btn btn-sm btn-primary">Generate Invoice</button>
					<button class="btn btn-sm">Change Order</button>
				</div>
			</div>
			<ProjectTimeline />
		</div>
	</div>
</details>

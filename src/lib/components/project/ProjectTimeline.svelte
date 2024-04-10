<script>
	import 'iconify-icon';
</script>

<ul class="timeline timeline-vertical timeline-snap-icon timeline-compact pl-10 xl:pl-16">
	<li>
		<div class="timeline-middle text-primary">
			<iconify-icon icon="lets-icons:check-fill" class="text-xl text-current"></iconify-icon>
		</div>
		<div class="timeline-end">
			<span class="badge badge-sm badge-primary">Approved</span>
			<details class="collapse collapse-arrow">
				<summary class="collapse-title text-lg font-medium">Requirements</summary>
				<div class="collapse-content">
					<p>content</p>
				</div>
			</details>
		</div>
		<hr class="bg-primary" />
	</li>
	<li>
		<hr class="bg-primary" />
		<div class="timeline-middle text-primary">
			<iconify-icon icon="lets-icons:check-fill" class="text-xl text-current"></iconify-icon>
		</div>
		<div class="timeline-end">
			<span class="badge badge-sm badge-primary">Approved</span>
			<details class="collapse collapse-arrow">
				<summary class="collapse-title text-lg font-medium">Project Plan</summary>
				<div class="collapse-content">
					<p>content</p>
				</div>
			</details>
		</div>
		<hr class="bg-primary" />
	</li>
	<li>
		<hr class="bg-primary" />
		<div class="timeline-middle text-primary">
			<iconify-icon icon="lets-icons:check-fill" class="text-xl text-current"></iconify-icon>
		</div>
		<div class="timeline-end">
			<span class="badge badge-sm badge-primary">Approved</span>
			<details class="collapse collapse-arrow">
				<summary class="collapse-title text-lg font-medium">Checkpoint 1</summary>
				<div class="collapse-content">
					<p>content</p>
				</div>
			</details>
		</div>
		<hr class="bg-primary" />
	</li>
	<li>
		<hr class="bg-secondary" />
		<div class="timeline-middle text-secondary">
			<iconify-icon icon="lets-icons:check-fill" class="text-xl text-current"></iconify-icon>
		</div>
		<div class="timeline-end">
			<span class="badge badge-sm badge-secondary">Delivered</span>
			<details class="collapse collapse-arrow">
				<summary class="collapse-title text-lg font-medium">Checkpoint 2</summary>
				<div class="collapse-content">
					<p>content</p>
				</div>
			</details>
		</div>
		<hr />
	</li>
	<li>
		<hr />
		<div class="timeline-middle">
			<iconify-icon icon="lets-icons:check-fill" class="text-xl text-current"></iconify-icon>
		</div>
		<div class="timeline-end">
			<span class="badge badge-sm">On Hold</span>
			<details class="collapse collapse-arrow">
				<summary class="collapse-title text-lg font-medium">Final Deliverable</summary>
				<div class="collapse-content">
					<p>content</p>
				</div>
			</details>
		</div>
	</li>
</ul>

<style lang="postcss">
	.timeline-middle {
		@apply w-5 aspect-square overflow-hidden;
	}
</style>

<script>
	import 'iconify-icon';
</script>

<aside>
	<div class="rounded-lg bg-base-100 text-base-content flex flex-col gap-4 p-4 w-full">
		<div class="flex flex-col gap-2">
			<h4 class="text-sm font-semibold">Client</h4>
			<ul class="menu p-0">
				<li>
					<a href="/clients/visiondeck">
						<img src="https://visiondeck.io/images/mark.png" alt="visiondeck mark" class="w-8" />
						<span>VisionDeck</span>
					</a>
				</li>
			</ul>
		</div>
		<div class="flex flex-col gap-2">
			<div class="flex justify-between items-center">
				<h4 class="text-sm font-semibold">Contacts</h4>
				<button type="button" class="btn btn-xs btn-square btn-ghost">
					<iconify-icon icon="ph:plus"></iconify-icon>
				</button>
			</div>
			<ul class="menu p-0">
				<li>
					<a href="/user/dylan@dylangluck.com">
						<div class="avatar online placeholder">
							<div class="bg-neutral text-neutral-content rounded-full w-8">
								<span>DG</span>
							</div>
						</div>
						<span>dylan@dylangluck.com</span>
					</a>
				</li>
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
				<h4 class="text-sm font-semibold">Bookmarks</h4>
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
	</div>
</aside>

<div class="navbar bg-base-100 border-b border-base-300 p-3">
	<div class="flex-1">
		<label for="app-drawer" class="btn btn-ghost drawer-button lg:hidden">
			<iconify-icon icon="material-symbols-light:menu" class="text-2xl"></iconify-icon>
		</label>
		<div class="form-control">
			<label class="input input-ghost flex items-center gap-2">
				<iconify-icon icon="material-symbols:search" class="text-2xl opacity-50"></iconify-icon>
				<input
					type="text"
					class="grow border-0 shadow-none"
					style="--tw-ring-shadow:transparent;"
					placeholder="Search"
				/>
				<kbd class="kbd kbd-xs max-lg:hidden opacity-50">⌘</kbd>
				<kbd class="kbd kbd-xs max-lg:hidden opacity-50">K</kbd>
			</label>
		</div>
	</div>
	<div class="flex-none gap-2">
		<div class="dropdown">
			<div tabindex="0" role="button" class="btn btn-sm">
				Theme
				<svg
					width="12px"
					height="12px"
					class="h-2 w-2 fill-current opacity-60 inline-block"
					xmlns="http://www.w3.org/2000/svg"
					viewBox="0 0 2048 2048"
					><path d="M1799 349l242 241-1017 1017L7 590l242-241 775 775 775-775z"></path></svg
				>
			</div>
			<!-- svelte-ignore a11y-no-noninteractive-tabindex -->
			<ul tabindex="0" class="dropdown-content z-[1] p-2 shadow-2xl bg-base-300 rounded-box w-52">
				<li>
					<input
						type="radio"
						name="theme-dropdown"
						class="theme-controller btn btn-sm btn-block btn-ghost justify-start"
						aria-label="Default"
						value="default"
					/>
				</li>
				<li>
					<input
						type="radio"
						name="theme-dropdown"
						class="theme-controller btn btn-sm btn-block btn-ghost justify-start"
						aria-label="Light"
						value="winter"
					/>
				</li>
				<li>
					<input
						type="radio"
						name="theme-dropdown"
						class="theme-controller btn btn-sm btn-block btn-ghost justify-start"
						aria-label="Dark"
						value="night"
					/>
				</li>
			</ul>
		</div>
		<div class="indicator mr-2">
			<span class="indicator-item badge-xs badge badge-secondary"></span>
			<button class="btn btn-sm">
				<iconify-icon icon="mdi:bell-outline" class="text-lg"></iconify-icon>
				<span class="max-md:sr-only">Inbox</span>
			</button>
		</div>
		<div class="avatar placeholder">
			<div class="bg-neutral text-neutral-content rounded-full w-8">
				<span>DG</span>
			</div>
		</div>
	</div>
</div>

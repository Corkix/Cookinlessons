<script lang="ts">
	import { page } from '$app/stores';
	import logo from '$lib/images/hagalogo1.png';

	// Skeleton Features
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import { Drawer, drawerStore } from '@skeletonlabs/skeleton';
	import { popup } from '@skeletonlabs/skeleton';
	import type { PopupSettings } from '@skeletonlabs/skeleton';
	import { ListBox, ListBoxItem } from '@skeletonlabs/skeleton';

	// Floating UI
	import { computePosition, autoUpdate, offset, shift, flip, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	storePopup.set({ computePosition, autoUpdate, offset, shift, flip, arrow });

	// Local Features
	import Navigation from '$lib/components/Navigation.svelte';

	// Stylesheets
	import '../theme.css';
	import '@skeletonlabs/skeleton/styles/all.css';
	import '../app.postcss';

	function drawerOpen(): void {
		drawerStore.open({});
	}

	let comboboxValue: string;

	const popupCombobox: PopupSettings = {
		event: 'focus-click',
		target: 'popupCombobox',
		placement: 'bottom',
		closeQuery: '.listbox-item'
	};

	// Reactive Properties
	$: classesSidebarLeft = $page.url.pathname === '/' ? 'w-0' : 'w-0 lg:w-64';
</script>

<!-- Drawer -->
<Drawer>
	<div class="flex">
		<div class="btn btn-sm">
			<img src={logo} alt="" />
		</div>
		<h2 class="p-4">Hagablänket</h2>
	</div>
	<hr />
	<Navigation />
</Drawer>

<!-- App Shell -->
<AppShell slotSidebarLeft="bg-surface-500/50 {classesSidebarLeft}">
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar class="drop-shadow-[0_1.2px_2.2px_rgba(0,0,0,0.8)]">
			<svelte:fragment slot="lead">
				<div class="flex items-center">
					<button class="lg:hidden btn btn-sm mr-4" on:click={drawerOpen}>
						<span>
							<svg viewBox="0 0 100 80" class="fill-token w-4 h-4">
								<rect width="100" height="20" />
								<rect y="30" width="100" height="20" />
								<rect y="60" width="100" height="20" />
							</svg>
						</span>
					</button>
					<div class="btn btn-sm justify-end">
						<img src={logo} alt="" />
					</div>
				</div>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<div class="max-sm:hidden">
					<a class="btn btn-sm text-lg" href="/">Hem</a>
					<button class="btn text-lg justify-between" use:popup={popupCombobox}>
						<span class="capitalize">{comboboxValue ?? 'Uthyrning'}</span>
					</button>
					<div class="card w-40 shadow-xl py-2" data-popup="popupCombobox">
						<ListBox rounded="rounded-none">
							<ListBoxItem bind:group={comboboxValue} name="Sjömagasinet" value="sjohus">
								<a class="btn btn-sm text-lg hover:text-slate-950" href="/sjohus">Sjömagasinet</a
								></ListBoxItem
							>
							<ListBoxItem bind:group={comboboxValue} name="Skogslugnet" value="skoghus">
								<a class="btn btn-sm text-lg hover:text-slate-950" href="/skoghus">Skogslunget</a>
							</ListBoxItem>
							<ListBoxItem bind:group={comboboxValue} name="Kontakt" value="kontakt">
								<a class="btn btn-sm text-lg hover:text-slate-950" href="/uthyrning">Kontakt</a>
							</ListBoxItem>
						</ListBox>
					</div>

					<a class="btn btn-sm text-lg" href="/njutbart">Njutbart</a>
					<a class="btn btn-sm text-lg" href="/omOss">Om oss</a>
					<a class="btn btn-sm text-lg" href="/stenberga">Missonsförsamiling</a>
				</div>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>

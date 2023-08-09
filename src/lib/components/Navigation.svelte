<script lang="ts">
	import { drawerStore } from '@skeletonlabs/skeleton';

	import { Accordion, AccordionItem } from '@skeletonlabs/skeleton';

	function drawerClose(): void {
		drawerStore.close();
	}
</script>

<nav class="list-nav p-4">
	<Accordion>
		<ul>
			<li><a href="/" on:click={drawerClose}>Hem</a></li>
			<AccordionItem>
				<svelte:fragment slot="summary">Uthyrning</svelte:fragment>
				<svelte:fragment slot="content">
					<ul>
						<li><a href="/sjohus" on:click={drawerClose}>Sjömagasinet</a></li>
						<li><a href="/skoghus" on:click={drawerClose}>Skogslunget</a></li>
						<li><a href="/kontakt" on:click={drawerClose}>Kontakt</a></li>
					</ul>
				</svelte:fragment>
			</AccordionItem>
			<li><a href="/omOss" on:click={drawerClose}>Njutbart</a></li>
			<li><a href="/omOss" on:click={drawerClose}>Om oss</a></li>
			<li><a href="/stenberga" on:click={drawerClose}>Missionsförsamling</a></li>
		</ul>
	</Accordion>
</nav>

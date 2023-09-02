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
			<li><a href="/uthyrning" on:click={drawerClose}>Uthyrning</a></li>
			<li><a href="/omOss" on:click={drawerClose}>Njutbart</a></li>
			<li><a href="/omOss" on:click={drawerClose}>Om oss</a></li>
			<li><a href="/stenberga" on:click={drawerClose}>Missionsförsamling</a></li>
		</ul>
	</Accordion>
</nav>

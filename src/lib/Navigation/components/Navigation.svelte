<script lang="ts">
	import { drawerStore } from '@skeletonlabs/skeleton';

	function drawerClose(): void {
		drawerStore.close();
	}
</script>

<nav class="list-nav p-4">
	<ul>
		<li><a href="/" on:click={drawerClose}>Hem</a></li>
		<li><a href="/uthyrning" on:click={drawerClose}>Uthyrning</a></li>
		<li><a href="/omOss" on:click={drawerClose}>Om oss</a></li>
		<li><a href="/stenberga" on:click={drawerClose}>Stenberga Missionsförsamling</a></li>
	</ul>
</nav>

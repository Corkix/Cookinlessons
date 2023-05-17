<script lang="ts">
	import { drawerStore } from '@skeletonlabs/skeleton';

	function drawerClose(): void {
		drawerStore.close();
	}
</script>

<nav class="list-nav p-4">
	<ul>
		<li><a href="/" on:click={drawerClose}>Home</a></li>
		<li><a href="/about" on:click={drawerClose}>Menu</a></li>
		<li><a href="/blog" on:click={drawerClose}>Reserve a Table</a></li>
		<li><a href="/contact" on:click={drawerClose}>Cooking Lessons</a></li>
	</ul>
</nav>

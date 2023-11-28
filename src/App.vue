<script>
import Navbar from './components/Navbar.vue';
import Library from './components/Library.vue';
import QuickLinks from './components/QuickLinks.vue';
export default {
	components: {
		Navbar,
		Library,
		QuickLinks
	}
}
</script>

<template>
	<header>
		<Navbar />
	</header>

	<main>
		<Library />
		<QuickLinks />
	</main>
</template>

<style scoped></style>

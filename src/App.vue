<script>
import Navbar from './components/Navbar.vue';
import Library from './components/Library.vue';
import QuickLinks from './components/QuickLinks.vue';
import JumboFooter from './components/JumboFooter.vue';
export default {
	components: {
		Navbar,
		Library,
		QuickLinks,
		JumboFooter
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

	<footer>
		<JumboFooter />
	</footer>
</template>

<style scoped></style>

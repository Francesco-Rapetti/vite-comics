<script>
import Navbar from './components/Navbar.vue';
import Library from './components/Library.vue';
export default {
	components: {
		Navbar,
		Library
	}
}
</script>

<template>
	<header>
		<Navbar />
	</header>

	<main>
		<Library />
	</main>
</template>

<style scoped></style>

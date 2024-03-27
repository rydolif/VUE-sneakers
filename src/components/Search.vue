<!-- Search.vue -->
<script setup>
	import { ref, defineProps, defineEmits } from 'vue'

	const props = defineProps({
		searchQuery: String,
	})

	const emits = defineEmits(['update:searchQuery'])

	const localSearchQuery = ref(props.searchQuery)

	const emitSearchQuery = () => {
		emits('update:searchQuery', localSearchQuery.value)
	}
</script>

<template>
	<div class="cards__search question__form">
		<div class="question__form_line">
			<input v-model="localSearchQuery" type="text" placeholder="Search" @input="emitSearchQuery" />
		</div>
	</div>
</template>

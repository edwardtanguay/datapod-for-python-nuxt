<script setup>
// const response = await $fetch("/api/flashcards");
import flashcards from '../../parseddata/flashcards.json'
</script>

<template>
	<p class="mb-4">Welcome to this site.</p>
	<p class="text-xl mb-3">
		There are {{ flashcards.length }} flashcards:
	</p>
	<div v-for="card in flashcards"
		 :key="card.suuid"
		 class="flex flex-col gap-1 p-3 mb-3 w-fit bg-slate-500 rounded">
		<div>
			<h3 class="font-semibold">{{ card.front }}</h3>
			<p class="text-yellow-200">{{ card.back }}</p>
		</div>
	</div>
</template>

<template>
	<main>
		<div class="text-center border-0 my-5">
			<img
				:alt="`${selectedUser.firstName} ${selectedUser.lastName}`"
				:title="`${selectedUser.firstName} ${selectedUser.lastName}`"
				class="card-img w-auto p-1 shadow-sm border rounded-circle mb-3 border-primary"
				:src="selectedUser.picture"
				v-if="selectedUser.picture"
			/>

			<h5 class="card-title mb-2">
				{{ selectedUser.firstName }}
				{{ selectedUser.lastName }}
			</h5>
			<p><strong>Phone#:</strong> {{ selectedUser.phone }}</p>
		</div>
	</main>
</template>

<script>
import { mapState } from 'vuex';

export default {
	computed: {
		...mapState(['selectedUser', 'searchResults'])
	}
};
</script>

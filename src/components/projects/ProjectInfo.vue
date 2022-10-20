<script>
import feather from 'feather-icons';

export default {
	props: ['projectInfo'],

	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
};
</script>

<template>
	<div class="block sm:flex gap-0 sm:gap-10 mt-14">
		<!-- Single project right section details -->
		<div class="w-full text-left">
			<p
				class="font-general-medium text-primary-dark dark:text-primary-light text-2xl font-bold mb-7"
			>
				{{ projectInfo.projectDetailsHeading }}
			</p>
			<p
				v-for="projectDetail in projectInfo.projectDetails"
				:key="projectDetail.id"
				class="font-general-regular mb-5 text-lg text-ternary-dark dark:text-ternary-light"
			>
				{{ projectDetail.details }}
			</p>
		</div>
	</div>
</template>

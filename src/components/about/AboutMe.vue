<script>
export default {
	setup() {
		return {
			bios: [
				{
					id: 1,
					bio:
						'HI, I am Willyta Asmara Diya Abadi!',
				},
				{
					id: 2,
					bio:
						'I am a human being who usually stays on the computer to write some programs. I really like things related to front-end web desaign, responsible for designing and building various web applications in a responsive, interactive, and user friendly way. With responsibility and discipline can bring up a motivated attitude and a variety of strong skills. Very good at time management on the job and in improving soft skills in technology and design. Highly organized, and skilled in written and verbal communication.',
				},
			],
		};
	},
};
</script>

<template>
	<div class="block sm:flex sm:gap-10 mt-10 sm:mt-20">
		<!-- About profile image -->
		<div class="w-full sm:w-1/4 mb-7 sm:mb-0">
			<img
				src="@/assets/images/profile.jpg"
				class="rounded-xl w-96"
				alt=""
			/>
		</div>

		<!-- About details -->
		<div class="w-full sm:w-3/4 text-left">
			<p
				v-for="bio in bios"
				:key="bio.id"
				class="font-general-regular mb-4 text-ternary-dark dark:text-ternary-light text-lg"
			>
				{{ bio.bio }}
			</p>
		</div>
	</div>
</template>

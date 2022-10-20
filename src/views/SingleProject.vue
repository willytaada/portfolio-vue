<script>
import feather from 'feather-icons';
import ProjectHeader from '../components/projects/ProjectHeader.vue';
import ProjectGallery from '../components/projects/ProjectGallery.vue';
import ProjectInfo from '../components/projects/ProjectInfo.vue';
// import projects from '../data/projects.js';

export default {
	name: 'Projects',
	components: {
		ProjectHeader,
		ProjectGallery,
		ProjectInfo,
	},
	data: () => {
		return {
			singleProjectHeader: {
				singleProjectTitle: "Project Website Penyedia Jasa (Loker Online)",
			},
			projectImages: [
				{
					id: 1,
					title: 'SDF Cambodia',
					img: require('@/assets/images/ui-project-1.jpg'),
				}
			],
			projectInfo: {
				projectDetailsHeading: 'Challenge',
				projectDetails: [
					{
						id: 1,
						details:
							'Tens of thousands of Cambodia’s young population enter the labor force each year. Labor force participation among the working age population (15–64 years) increased from 7.7 million in 2009 to 8.3 million in 2015. While the country is endowed with an ample supply of labor, the labor force is still characterized by very low levels of education and skill. The average educational attainment of the current workforce is primary school completion (grade 6) or below—a major barrier to industrial diversification efforts and moving up the value chain. The 2015 Cambodia Socio-Economic Survey found that nearly half (46%) of the labor force have either not completed primary education or never attended school. Less than 7% of workers completed high school (grade 12). There is a pressing need to respond to the growing demand for an adaptable workforce with professional skills and proper workplace behavior. In response, the government has taken steps to reform and strengthen the education and training system, including an enhanced role of the private sector in skills development and providing incentives to enterprises to train their own workforce. The pilot Skills Development Fund (SDF) is an industry-driven workforce development program. The general notion is to build confidence in industry partnership and to engage more strongly with the private sector and their training needs. Firms willing but at times hesitant to further develop their workforce may be supported by the SDF to further invest in workforce development. Motivated private workforce development initiatives and intentions shall be mainly supported by the SDF (which in turn consists of a motivated, skilled, and client-oriented team).',
					},
				],
			},
		};
	},
	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
	methods: {},
};
</script>

<template>
	<div class="container mx-auto mt-10 sm:mt-20">
		<!-- Project header -->
		<ProjectHeader :singleProjectHeader="singleProjectHeader" />

		<!-- Project gallery -->
		<ProjectGallery :projectImages="projectImages" />

		<!-- Project information -->
		<ProjectInfo :projectInfo="projectInfo" />
	</div>
</template>

<style scoped></style>

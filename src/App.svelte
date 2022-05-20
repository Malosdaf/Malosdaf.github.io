<script>
	import { reveal } from "svelte-reveal";

	import Background from "./Background.svelte";
	import Next_Background from "./Next-Background.svelte";
	import Logo from "./Logo.svelte";
	import ScrollHint from "./ScrollHint.svelte";
	import About from "./Bio.svelte";
	import FullScreenContainer from "./FullScreenContainer.svelte";
	import Destiny2Profile from "./Destiny2Profile.svelte";
	import CoolPeople from "./CoolPeople.svelte";
	import Credits from "./Credits.svelte";
	import Achievement from "./Achievement.svelte";
	import Project from "./Project.svelte";
</script>

<main>
	<Next_Background/>
	<ScrollHint/>

	<!-- content -->
	<div class="md:m-auto md:w-3/4">
		<Logo/>

		<div class="w-full flex flex-col items-center p-8">
			<!-- self promotion -->
			<FullScreenContainer>
				<h3 use:reveal>Bio</h3>
				<About/>
			</FullScreenContainer>
			<FullScreenContainer>
				<h3 use:reveal>Project</h3>
				<Project name="Malosdaf"/>
			</FullScreenContainer>
	`		<FullScreenContainer>
			<h3 use:reveal>Achievement</h3>
				<Achievement/>
			</FullScreenContainer>
			<!-- games -->
			<FullScreenContainer>
				<h3 use:reveal>Game profiles</h3>
				<Destiny2Profile id="19700278"/>
			</FullScreenContainer>

			<!--<FullScreenContainer>-->
			<!--	<h3 use:reveal>Cool people</h3>-->
			<!--	<CoolPeople/>-->
			<!--</FullScreenContainer>-->

			<FullScreenContainer>
				<h3 use:reveal>Credits</h3>
				<Credits/>
			</FullScreenContainer>
		</div>
	</div>
</main>
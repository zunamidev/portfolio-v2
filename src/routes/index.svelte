<script lang="ts">
    import Navigation from '$lib/sections/navigation.svelte'
    import Header from '$lib/sections/header.svelte'
    import AboutSection from '$lib/sections/about.svelte'
    import ProjectSection from '$lib/sections/projects.svelte'
    import SkillSection from '$lib/sections/skills.svelte'
    import Wave from '$lib/components/wave.svelte'
</script>

<Navigation></Navigation>
<Header></Header>
<main>
    <Wave></Wave>
    <AboutSection></AboutSection>
    <Wave flip={true}></Wave>
    <ProjectSection></ProjectSection>
    <Wave></Wave>
    <SkillSection></SkillSection>
    <Wave flip={true}></Wave>
</main>
<footer></footer>

<style lang="scss">
    main {
        display: flex;
        flex-direction: column;
    }

    :global {
        .container {
			padding-left: 5vw;
			padding-right: 5vw;

            h1 {
                font-size: 48px;
            }
		}
    }
</style>
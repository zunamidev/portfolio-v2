<script lang="ts">
    import Project from '$lib/components/project.svelte'
    // import fetch from 'node-fetch'
    import { onMount } from 'svelte';

    let repos = []

    onMount(async () => {
        const res = await fetch(`https://api.github.com/users/zunamidev/repos?per_page=8`);
		repos = await res.json();
    });
</script>
<section id="projects">
    <div class="container">
        <h1>Projects</h1>
        <div class="projects-list">
            {#each repos as item, i }
            <Project name={item.name} language={item.language} url={item.html_url}></Project>
            {/each}
        </div>
    </div>
</section>
<style lang="scss">
    section{
        .container {
            h1 {
                font-size: 48px;
            }
        }
        .projects-list {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            gap: 10px;
        }
    }

    @media screen and (max-width: 768px) {
        section {
            .projects-list {
                grid-template-columns: 1fr 1fr;
                gap: 20px;
            }
        }

    }
</style>
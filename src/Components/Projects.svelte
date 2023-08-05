<script>
    import {projects} from "../InfoData/projects";
	import ProjectCard from "./ProjectCard.svelte";
</script>

<div class="projects" id="projects">
    <h2>Projects</h2>
    {#each projects as project }
        <ProjectCard project={project}/>
    {/each}

</div>

<style>
.projects{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 20px;
    gap: 20px;
}

.projects h2{
    color: var(--tertiary-color);
}
</style>

<script>
import SkillsCard from "./skillsCard.svelte";
import {skillsList} from "../InfoData/skills";
</script>

<div class="skills" id="skills">
  <h2>Tech Skills</h2>
  <div class="skillCardContainer">
  {#each skillsList as skill}
  
   <SkillsCard skillName={skill.name} icon={skill.icon}/>

  {/each}
</div>
</div>

<style>
    .skills{
        
        width: 70%;
        margin: 100px auto;
         padding: 10px;
         display: flex;
         flex-direction: column;
         align-items: center;
         gap: 20px;
         
    }

    .skills h2
    {
        color: var(--tertiary-color);
       font-size: 31px;
       
    }

    .skillCardContainer
    {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 20px;
        width: 100%;
      
        align-items: center;
        justify-items: center;
    }


    @media (max-width:650px)
    {
        .skillCardContainer{
            grid-template-columns: 1fr;
        }
    }
</style>
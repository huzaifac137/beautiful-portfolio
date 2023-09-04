
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
        
        width: 90%;
        margin :150px auto;
         padding: 10px;
         display: flex;
         flex-direction: column;
         align-items: center;
         gap: 20px;

         animation: slideInLeft 1s ease 0s;
         
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
         place-items: center;
    }





</style>
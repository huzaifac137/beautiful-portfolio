<script>
    export let skillName ,icon;
</script>

<div class="skillCard">
   <h3>{skillName}</h3>
    <img src={icon} height="50" width="50" alt="skill-icon"  />
</div>

<style>
.skillCard{
   display: flex;
   flex-direction: column;
   align-items: center;
   gap: 10px;
   padding: 10px;
   border-bottom: 1px solid var(--secondary-color);
   border-radius: 4px;
   
   
}

.skillCard h3
{
    color: var(--secondary-color);
}


</style>
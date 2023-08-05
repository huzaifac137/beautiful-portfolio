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
   width: 38%;
   border-bottom: 1px solid var(--tertiary-color);
   border-radius: 3px;
   padding: 10px;
   
}

.skillCard h3
{
    color: var(--secondary-color);
}


</style>
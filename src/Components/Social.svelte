<script>
import {socialLinks} from "../InfoData/social"
</script>

<div class="social">

  <div class="socialContainer" >
   {#each socialLinks as Link }
   <a href={Link.url} target="_blank" >
   <img src={Link.icon} height="25" width="25" alt="social media icons"  />
   </a>  
   {/each}
  </div>
</div>

<style>
    .social {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-top: 20px;
        gap: 20px; 
        margin-top: 70px;
    }

    .social h2{
        color: var(--tertiary-color);
    }

    .socialContainer{
        display: flex;
        align-items: center;
        justify-content: center;
        width: 50%;
        margin-bottom: 10px;
        cursor: pointer;
        gap:20px;
    }

    @media (max-width:650px){
        .socialContainer{
            width: 80%;
        }
    }
</style>
<script>
 let open = false;

 const handleHamBurger=()=>{
    open = !open;
 }

</script>

<div class={open===true ? "hamburger-open" : "header"}>
    <button class="spanContainer" on:click={handleHamBurger}>
    <span class="span"> </span>
    <span class="span"> </span>
    <span class="span"> </span>
    </button>
  <a href="#" on:click={handleHamBurger}>Home</a>
   
     <a href="#skills" on:click={handleHamBurger}>Skills</a>
      <a href="#projects" on:click={handleHamBurger}>Projects</a>
</div>

<style>

.header , .hamburger-open{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-evenly;
    margin-top: 16px;

}


.spanContainer{
    display: none;
}

.header a , .hamburger-open a{
    cursor: pointer;
    color: var(--secondary-color);
    text-decoration: none;
}

.header a:hover
{
    color:var(--tertiary-color)
}

@media(max-width:650px)
{

    .header{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        
    }
    .header a{
        display: none;
    }

    .hamburger-open{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        height: auto;
        margin-top: 16px;
       
    }

    .hamburger-open a{
        align-self: center; 
        cursor: pointer;
       color: var(--secondary-color);
         text-decoration: none;
         margin-top: 15px;
        
             }

    .span{
        height: 3px;
        width: 30px;
        
        background-color: aliceblue;
    }

    .spanContainer{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        margin-left: 10px;
        gap: 7px;
        background-color: transparent;
        border: none;
    }


}
</style>
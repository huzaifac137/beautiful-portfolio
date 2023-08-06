<script>
    export let project;
</script>

<div class="flip-card">
    <div class="flip-card-inner">
        <div class="flip-card-front">
         
            <p class="title">{project.title}</p>
            <p class="open-more">More info</p>
        </div>
        <div class="flip-card-back">
            <div class="flip-card-tooltech">
                {#each project.toolsntech as toolntech }
                <img src={toolntech} alt={project.title} width="30" height="30"/>
             {/each}
            </div>
            <p class="desc">{project.description}</p>
            
        </div>
    </div>
</div>

<style>
.flip-card {

  background-color: transparent;
  width: 40%;
  height: 254px;
  perspective: 1000px;
  font-family: sans-serif;
  padding: 10px;
}

.title {
  font-size: 17px;
  font-weight: 900;
  text-align: center;
  margin: 0;
}

.open-more{
    font-size: 14px;
    color: var(--secondary-color);
}

.desc {
  font-size: 13px;
  font-weight: 300;
  text-align: center;
  margin: 0;
}


.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

.flip-card-tooltech{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 10px;
}

.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

.flip-card-front, .flip-card-back {
  box-shadow: 0 8px 14px 0 rgba(0,0,0,0.2);
  position: absolute;
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;

  border-radius: 1rem;
}

.flip-card-front {
  background: transparent;
  color: var(--tertiary-color);
  border: 1px solid var(--secondary-color);
}

.flip-card-back {
  background: var(--tertiary-color) ;
  color: var(--secondary-color);
  transform: rotateY(180deg);
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 10px;
  gap: 10px;
}

@media (max-width:900px)
{
    .flip-card{
        width: 60%;
    }
}

@media (max-width:650px)
{
    .flip-card
    {
        width: 70%;
    }
}

</style>
<script>
    import Button from "./shared/Button.svelte";
    import Subtitle from "./shared/Subtitle.svelte";
    import cardOne from "../static/image-del-sol.jpg";
    import cardTwo from "../static/image-228b.jpg";
    import cardThree from "../static/image-prototype.jpg";

    const cardsData = [
        { text: "Project Del Sol", img: cardOne },
        { text: "228B Tower", img: cardTwo },
        { text: "Le Prototype", img: cardThree },
    ];
</script>

<div class="featured">
    <div class="featured__title">
        <!-- <h4>Featured</h4> -->
        <Subtitle color="dark">
            <span>Featured</span>
        </Subtitle>
        <Button>
            <span slot="text">See All &rarr;</span>
        </Button>
    </div>
    <div class="featured__cards">
        {#each cardsData as currentCard}
        <!-- trop de boilerplate pour le code dessous -->
        <!-- utiliser ce lien pour essayer de le reparer: https://stackoverflow.com/questions/57174373/can-i-set-svelte-style-css-attribute-values-using-variables-passed-in-to-a-compo -->
             <figure style="background-image: linear-gradient(to bottom, rgba(0,0,0, 0.7), rgba(0,0,0, 0.4)), url({currentCard.img})" class="card">
                <h4>{currentCard.text}</h4>
                <p>View All Projects</p>
             </figure>
        {/each}
    </div>
</div>

<style>
    .featured {
        margin-bottom: 15rem;
    }
    
    .featured__title {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .featured__cards {
        height: 65vh;
        display: grid;
        grid-template-columns: repeat(3, 50rem);
        column-gap: 4rem;
    }

    .card {
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        align-items: center;
        background-repeat: no-repeat;
        background-size: cover;
        padding-bottom: 5rem; /* works parfaitement, ainsi, flex-end ne fait pas coller le texte vers dessous. il donne un peu d'espece */
        /* background-image: linear-gradient(to bottom, rgba(0,0,0, 0.7), rgba(0,0,0, 0.4)); */

    }

    .card > * {
        color: #EEEFF4;
    }

    .card h4 {
        font-size: 3.5rem;
    }

    .card p {
        font-size: 2rem;
    }
</style>

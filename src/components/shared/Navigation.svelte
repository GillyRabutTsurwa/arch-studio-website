<script>
    import { url } from '@roxi/routify';
    export let pageTitle;
    
    let pageNames = ["portfolio", "about", "contact"];

    const capitalise = (string) => string.charAt(0).toUpperCase() + string.slice(1);
    
</script>

<nav class="navigation">
    <p class="indicator">{pageTitle}</p>
    <h1>
        <a href={$url("./")}>Arch</a>
    </h1>
    <ul class="navigation__list">
        {#each pageNames as currentName}
        <li class="navigation__list--item">
            <a href={$url(`./${currentName}`)}>{capitalise(currentName)}</a>
        </li>
        {/each}
    </ul>
</nav>



<style>
    .indicator {
    position: absolute; /* le parent c'est le tag body. because of position absolute. it's not in flex flow (what we want) and is still related to body tag with position relative */
    writing-mode: vertical-rl;
    top: 9rem;
    left: 4%;
    text-transform: uppercase;
    color: #BBB;
}

.indicator::before {
    content: "";
    position: absolute;
    top: -14.5rem;
    right: 0.75rem;
    width: 1px;
    height: 11.5rem;
    border: 1px solid currentColor;

}


.navigation,
.navigation__list {
    display: flex;
}

.navigation {
    align-items: center;
    margin: 3.5rem 0;
}

h1 {
    margin-right: 2.5rem;
    font-size: 6rem;
}

.navigation__list {
    list-style:none;
}

.navigation__list--item {
    margin-right: 4rem;
}
</style>
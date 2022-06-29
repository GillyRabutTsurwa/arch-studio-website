<script>
    import Button from "./shared/Button.svelte";
    import photo from "../static/image-hero-paramour.jpg";

</script>

<header class="header">
    <figure class="header__img-area">
        <div class="header__title-n-text">
            <h2 class="header__title">Project Paramour</h2>
            <p class="header__text">
                <span>Project made for an art museum near Southwest London,</span>
                <span>Project Paramour is a statement of bold, modern architecture</span>
            </p>
            <Button/>
        </div>
        <ul class="header__carousel-btn__list">
            {#each Array(4) as _, index}
                <li><span>{index + 1}</span></li>
            {/each}
        </ul>
    </figure>
</header>


<style>
    .header {
         width: 100%;
         margin-bottom: 20rem;
    }

    .header figure {
        position: relative;
        width: 100%;
        height: 80vh;
        background-image: linear-gradient(to right, rgba(0,0,0, 0.7), rgba(0,0,0, 0.4)), url(../static/image-hero-paramour.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center center;
    }

    .header__title {
        font-size: 9.6rem;
        margin-bottom: 2rem;
    }

    .header__text {
        font-size: 2rem;
        margin-bottom: 2rem;
    }

    .header__text span {
        display: block;
        line-height: 1.5;
    }

    .header__img-area div {
        position: absolute;
        top: 30%;
        left: 15%;
        color: #fff;
    }

    .header__img-area .header__carousel-btn__list {
        position: absolute;
        bottom: -0.4rem;
        font-weight: 500;
        /* TESTING */
        display: flex;
    }

    .header__img-area .header__carousel-btn__list li {
        position: relative;
        display: inline-block;
        width: 6.5rem;
        height: 6.5rem;
        background-color: #fff;
        color: #333;
        cursor: pointer;
    }

    .header__img-area .header__carousel-btn__list li span {
        
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
</style>
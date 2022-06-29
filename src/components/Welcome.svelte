<script>
    import photo from "../static/image-welcome.jpg";
    import Button from "./shared/Button.svelte";
    import Subtitle from "./shared/Subtitle.svelte";
</script>

<div class="welcome">
    <h3 class="title-huge">Welcome</h3>
    <h4 class="title-regular">Welcome to Arch Studio</h4>
    <div class="text">
        <p>We have a unique network and skillset to help bring your projects to life. Our small team of highly skilled individuals combined with our large network put us in a strong position to deliver exceptional results
        </p>
        <p>Over the past 10 years, we have worked on all kinds of projects. From stations to high-rise buildings, we create spaces that inspire and delight
        </p>
        <p>
            We work closely with our clients so that we understand the intricacies of each project. This allows us to work in harmony in the surrounding area to create truly stunning projects that will stand the test of time
        </p>
    </div>
    <figure class="test">
        <img src={photo} alt="">
    </figure>
</div>
<!-- j'ai decidé de le mettre ici -->
<figure class="small-team">
    <div>
        <Subtitle color="light">
            <span>Small team,</span>
            <span>big ideas</span>
        </Subtitle>
        <Button>
            <span slot="text">About Us &rarr;</span>
        </Button>
    </div>
</figure>

<style>
    .welcome {
        display: grid;
        grid-template-columns: min-content 1fr;
        grid-template-rows: repeat(2, min-content) 1fr;
    }
    h3 {
        font-size: 25.5rem;
        color: #ccc;
        grid-column: 1 / 2;
        grid-row: 1 / 2;
        z-index: 1000;
        position: relative;
        transform: translate(15%, -50%);
        align-self: start;
    }
    h4 {
        grid-column: 1 / 2;
        grid-row: 2 / 3;
        transform: translate(25%, -17.5rem);
        position: relative;
        
        font-size: 6rem;
    }
    .text {
        grid-column: 1 / 2;
        grid-row: 3 / 4;
        font-size: 2.5rem;
        line-height: 1.5;
        transform: translateY(-20%);

    }

    .text p {
        width: 50%;
        position: relative;
        transform: translateX(50%);
        margin-bottom: 3rem;
    }

    .test {
        grid-column: 2 / 3;
        grid-row: 1 / span 3;
    }

    .test img {
        width:100%;height:100%;
    }

    .small-team {
        position: relative;
        width: 100%;
        height: 60vh;
        background-image: linear-gradient(to right, rgba(0,0,0, 0.5), rgba(0,0,0, 0.7)), url("../static/image-small-team.jpg");
        background-repeat: no-repeat;
        background-size: cover;
        margin-top: 25rem;
        margin-bottom: 15rem;

    }

    .small-team div {
        position: absolute;
        top: 40%;
        left: 17.25%;
    }

    .small-team div h5 {
        font-size: 8rem;
        color: #fff;
    }

    /* le composant Subtitle est un h2, voici pourquoi le code ci-dessous marche bien */
    .small-team div h2 span {
        display: block;
    }

    /* span {
        display: block;
    } */
</style>
<script>
    import { url } from '@roxi/routify';
    import photo from "../static/image-hero-paramour.jpg";

</script>

<header class="header">
    <p class="indicator">home</p>
    <div>
        <nav class="navigation">
            <h1>Arch</h1>
            <ul class="navigation__list">
                <li class="navigation__list--item">
                    <a href={$url("./portfolio")}>Portfolio</a>
                </li>
                <li class="navigation__list--item">
                    <a href={$url("./about")}>About Us</a>
                </li>
                <li class="navigation__list--item">
                    <a href={$url("./contact")}>Contact</a>
                </li>
            </ul>
        </nav>
        
        <figure>
            <div>
                <h2>Project Paramour</h2>
                <p>Project made for an art museum near Southwest London,</p>
                <p>Project Paramour is a statement of bold, modern architecture</p>
                <button>See Our Portfolio &rarr;</button>
            </div>
            <ul>
                <li><span>01</span></li><li><span>02</span></li><li><span>03</span></li><li><span>04</span></li>
            </ul>
        </figure>
    </div>
</header>


<style>
    .indicator {
        position: relative;
        writing-mode: vertical-rl;
        right: 6.5%;
        top: 14rem;
        text-transform: uppercase;
        color: #BBB;
    }

    .indicator::before {
        content: "";
        position: absolute;
        top: -14.5rem;
        right: 0.75rem;
        width: 1px;
        height: 10.5rem;
        border: 1px solid currentColor;

    }

    .header {
         width: 100%;
         margin-bottom: 20rem;
    }

    .navigation,
    .navigation__list {
        display: flex;
    }

    .navigation {
        align-items: center;
        margin-bottom: 2.5rem;

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

    .header figure {
        position: relative;
        width: 100%;
        height: 80vh;
        background-image: linear-gradient(to right, rgba(0,0,0, 0.5), rgba(0,0,0, 0.2)), url(../static/image-hero-paramour.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center center;
    }

    figure div {
        position: absolute;
        top: 30%;
        left: 15%;
        color: #fff;
    }

    figure ul {
        position: absolute;
        bottom: -0.4rem;
    }

    figure ul li {
        position: relative;
        display: inline-block;
        width: 6.5rem;
        height: 6.5rem;
        background-color: #fff;
        color: #333;
    }

    figure ul li span {
        
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
</style>
<script>
    import Button from "./shared/Button.svelte";
    import { url } from '@roxi/routify';
</script>

<footer class="footer">
    <nav class="footer-nav">
        <h4>Arch</h4>
        <ul class="footer-nav__list">
            <li class="footer-nav__list--item">
                <a href={$url("./portfolio")}>Portfolio</a>
            </li>
            <li class="footer-nav__list--item">
                <a href={$url("./about")}>About Us</a>
            </li>
            <li class="footer-nav__list--item">
                <a href={$url("./contact")}>Contact</a>
            </li>
        </ul>
    </nav>
    <!-- je vais addresser le code dessous plus tard -->
    <Button id="test" class="btn-footer"/>
</footer>

<style>
    .footer {
        position: relative;
        bottom: 0;
        width: 60vw;
        margin: 0 auto;
        display: flex;
        align-items: center;
    }

    .footer-nav {
        flex-grow: 2;
        display: flex;
        background-color: #eee;
    }

    .footer-nav__list {
        align-self: center;
        display: flex;
        justify-content: flex-start;
        width: 100%;
        margin-left: 3rem;
        list-style-type: none;
        color: #7D828F;
    }

    .footer-nav__list--item {
        margin-right: 4rem;
    }

    .footer-nav__list--item a:link,
    .footer-nav__list--item a:visited {
        text-decoration: none;
        color: #7D828F;
        border-bottom: 0.5px solid transparent;
        transition: all 0.5s ease-in;
    }

    .footer-nav__list--item a:hover,
    .footer-nav__list--item a:active {
        border-bottom: 0.5px solid currentColor;
    }

    .footer-nav h4 {
        background-color: #333;
        color: #fff;
        padding: 5rem;
        font-size: 4rem;
    }
</style>
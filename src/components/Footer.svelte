<script>
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
    <button>See Our Portfolio &rarr;</button>
</footer>

<style>
    .footer {
        position: relative;
        bottom: 0;
        width: 60vw;
        margin: 0 auto;
        display: flex;
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
    }

    .footer-nav__list li {
        margin-right: 3rem;
    }

    .footer-nav h4 {
        background-color: #333;
        color: #fff;
        padding: 5rem;
        font-size: 4rem;
    }

    .footer button {
        align-self: center;
    }
</style>
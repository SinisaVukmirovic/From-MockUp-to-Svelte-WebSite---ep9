<script>
    const navLinks = [
        { link: 'home' },
        { link: 'about' },
        { link: 'menu' },
        { link: 'reserve' },
        { link: 'gallery' },
        { link: 'contact' }
    ];
</script>

<style>
    footer {
        padding: 3em;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    
    img {
        margin-bottom: 3em;
    }

    p {
        letter-spacing: 3px;
        font-size: .7rem;
        color: var(--text-light);
    }

    span {
        letter-spacing: 3px;
        font-size: .7rem;
        color: var(--text-dark);
        margin-left: 1em;
    }

    .nav-links {
        display: flex;
        justify-content: center;
        margin: .75em 0 2em;
        padding: .5em;
        list-style: none;
    }
        .nav-links li {
            margin: 0 1em;
        }
    
        .nav-links a {
            font-size: .7rem;
            color: var(--text-clr);
            text-decoration: none;
            transition: color 250ms;
        }
        .nav-links a:hover {
            color: var(--theme-clr);
        }
    
    .logo {
            text-align: center;
        }
        .logo img {
            width: 65%;
            opacity: .4;
        }

    footer .text {
        display: flex;
        align-items: flex-end;
    }

    .copy {
        color: var(--text-dark);
        letter-spacing: 0;
    }

    @media only screen and (max-width: 768px) {
        footer {
            padding: 1em;
        }
        img {
            margin-bottom: 1.5em;
        }
        span {
            margin-left: .5em;
        }
        .nav-links {
            margin: .5em 0 1em;
            padding: .25em 0;
        }
        .nav-links li {
            margin: 0 .25em;
        }
    }
</style>

<!-- Mark Up -->
<footer id="contact">
    <div class="logo">
        <img src="img/logo.jpg" alt="Logo">
    </div>
    <div class="text">
        <p>+1 215 456 15 15.</p> <span>8:00 am - 11:30 pm</span>
    </div>
    <ul class="nav-links">
        {#each navLinks as { link }}
            <li>
                <a href="#{link}">{link}</a>
            </li>
        {/each}
    </ul>
    <p class="copy">Copyright &copy; 2019 | All rights reserved | MockUp to Svelte Website - ep9</p>
</footer>
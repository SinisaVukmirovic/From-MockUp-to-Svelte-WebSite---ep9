<script>
    const navLinks = [
        { link: 'home' },
        { link: 'about' },
        { link: 'menu' },
        { link: 'reserve' },
        { link: 'gallery' },
        { link: 'contact' }
    ];

    let active = navLinks[0];
</script>

<style>
    nav {
        height: 25vh;
        padding: 2em 5%;
        display: flex;
        flex-direction: column;
    }

    .logo-nav {
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
    }
        .logo {
            text-align: center;
        }
            .logo img {
                width: 70%;
            }

    .logo-nav .side {
        display: flex;
    }
        .side i {
            font-size: 2.25rem;
            margin: 0 .5em 0 0;
        }
        
        .side:last-child {
            text-align: right;
        }
            .side:last-child i {
                text-align: right;
                margin: 0 0 0 .5em;
            }
            .side:last-child span {
                cursor: pointer;
                transition: color 250ms;
            }
            .side:last-child span:hover {
                color: var(--theme-clr);
            }

        .side p {
            letter-spacing: 3px;
            font-size: .7rem;
            color: var(--text-light);
        }

        .side span {
            letter-spacing: 3px;
            font-size: .7rem;
            color: var(--text-dark);
        }

    .nav-links {
        display: flex;
        justify-content: center;
        margin-top: 1.5em;
        padding: 1em 0 .5em;
        list-style: none;
    }
        .nav-links li {
            margin: 0 1em;
            transition: all 250ms;
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
    
    li.active a {
        color: var(--theme-clr);
    }

    .fa-shopping-basket {
        position: relative;
    }
        .fa-shopping-basket::after {
            position: absolute;
            content: '3';
            top: 0;
            right: -.5em;
            width: 1rem;
            height: 1rem;
            border-radius: 50%;
            background-color: var(--theme-clr);
            color: #333;
            font-size: .8rem;
            display: flex;
            justify-content: center;
            align-items: center;
        }

    @media only screen and (max-width: 768px) {
        nav {
            height: 20vh;
            padding: 2em 10%;
            flex-direction: row;
            justify-content: space-between;
        }
        .logo img {
            width: 85%;
        }
        .logo-nav .side {
            display: none;
        }
        .nav-links {
            flex-direction: column;
            align-items: flex-end;
            margin-top: 1.5em;
            padding: 0;
        }
            .nav-links li {
                margin: 0;
            }
    }

    @media only screen and (max-height: 414px) {
        nav {
            height: 40vh;
        }
    }
</style>

<!-- Mark Up -->
<nav id="home">
    <div class="logo-nav">
        <div class="side">
            <i class="fas fa-mobile-alt"></i>
            <div>
                <p>+1 215 456 15 15</p>
                <span>8:00 am - 11:30 pm</span>
            </div>
        </div>
        <div class="logo">
            <img src="img/logo.jpg" alt="Logo">
        </div>
        <div class="side">
            <div>
                <p>$34.00</p>
                <span>3 items - view cart</span>
            </div>
            <i class="fas fa-shopping-basket"></i>
        </div>
    </div>

    <ul class="nav-links">
        {#each navLinks as link}
            <li
            class:active={active === link}
            on:click={() => active = link}
            >
                <a href="#{link.link}">{link.link}</a>
            </li>
        {/each}
    </ul>
</nav>
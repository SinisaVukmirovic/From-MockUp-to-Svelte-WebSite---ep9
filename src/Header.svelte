<style>
    header {
        height: 75vh;
        padding: 0 18%;
        background-image: url('img/cover.jpg');
        background-size: cover;
        background-position: center;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        position: relative;
    }
        header::after{
            background: 
					linear-gradient(-45deg, transparent 10px, var(--bg-clr) 0), 
					linear-gradient(45deg, transparent 10px, var(--bg-clr)  0);
            background-repeat: repeat-x;
            background-position: left top;
            background-size: 14px 20px;
            content: "";
            display: block;

            width: 100%;
            height: 20px;

            position: absolute;
            top: -10px;
            left: 0;
        }

    .title {
        border-bottom: 3px solid var(--text-clr);
    }
        .title h1,
        .title h2 {
            font-weight: lighter;
            color: var(--text-light);
            margin: 0 1em .25em 0;
        }
        .title h1 {
            font-size: 3rem;
            letter-spacing: 10px;
        }
        .title h2 {
            font-size: 1.5rem;
            letter-spacing: 5px;
        }

        p {
            color: var(--text-clr);
            margin: 2.75em 0 1.5em;
            letter-spacing: 2px;
        }

        .btn {
            padding: .75em .5em .75em 1em;
            font-size: .7rem;
            color: var(--text-light);
            text-transform: uppercase;
            text-decoration: none;
            letter-spacing: 2px;
            font-weight: bold;
            border: 2px solid var(--text-clr);
            margin-right: 1em;
            transition: all 250ms;
        }
            .btn:hover {
                background-color: var(--theme-clr);
                border: 2px solid var(--theme-clr);
                color: #333;
            }

            .btn:last-child {
                color: #333;
                background-color: var(--theme-clr);
                border: 2px solid var(--theme-clr);
            }
                .btn:last-child:hover {
                    color: var(--theme-clr);
                    background-color: transparent;
                }

    .fa-angle-right {
        margin-left: 1em;
    }

    @media only screen and (max-width: 768px) {
    header {
        height: 80vh;
        padding: 0 10%;
        background-image: url('img/cover.jpg');
        background-size: cover;
        background-position: center;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        position: relative;
    }
    .title h1, 
    .title h2 {
		letter-spacing: 5px;
	}
	.title h1 {
		font-size: 1.75rem;
	}
	.title h2 {
		font-size: 1.25rem;
    }
    
    @media only screen and (max-height: 414px) {
        header {
            height: 100vh;
        }
    }
}
</style>

<!-- Mark Up -->
<header>
    <div class="content">
        <div class="title">
            <h1>Vinsent Pizza.</h1>
            <h2>Making People Happy</h2>
        </div>
        <p>Italian pizza with cherry tomatoes and green basil</p>
        <a class="btn" href="#home">Order Now <i class="fas fa-angle-right"></i></a>
        <a class="btn" href="#home">View Menu <i class="fas fa-angle-right"></i></a>
    </div>
</header>
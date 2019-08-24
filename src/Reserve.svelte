<style>
    #reserve {
        padding: 5em 0;
        background-image: url('img/bg.jpg');
        background-size: cover;
        background-position: center;
    }

    form,
    .content {
        width: 40%;
        margin: 0 auto;
    }

    .content {
        color: var(--bg-clr);
        text-align: center;
    }
        .content h2 {
            color: var(--bg-clr);
            margin-top: .5em;
        }
        .content hr {
            margin: 2em auto;
        }

    .inputs {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-column-gap: 1em;
        grid-row-gap: .75em;
        margin: 3em 0 .75em;
    }
    
    textarea {
        width: 100%;
    }

    .btn {
        display: inline-block;
        margin: 1em 0 0 50%;
        transform: translateX(-50%);
        padding: .75em .5em .75em 1em;
        font-size: .7rem;
        color: var(--bg-clr);
        text-transform: uppercase;
        text-decoration: none;
        letter-spacing: 2px;
        font-weight: bold;
        border: 2px solid var(--bg-clr);
        transition: all 250ms;
    }
        .btn:hover {
            background-color: var(--bg-clr);
            color: var(--text-light);
        }

    @media only screen and (max-width: 768px) {
        #reserve {
            padding: 2em 10%;
        }
        form,
        .content {
            width: 100%;
        }
        .content hr {
            margin: 1em auto;
        }
        .inputs {
            grid-template-columns: repeat(1, 1fr);
            grid-row-gap: .5em;
            margin: 1em 0 .5em;
        }
    }
</style>

<!-- Mark Up -->
<section id="reserve">
    <div class="content">
        <h5>Not just a pizza, but lifestyle</h5>
        <h2>Make a Reservation</h2>
        <hr>
        <p>Lorem ipsum dolor sitsdfs amet consectetur adipisicing elit. Necessitatibus inventore possimus ea laboriosam rerum, vitae ducimus eum suscipit eos sapiente?</p>
    </div>

    <form>
        <div class="inputs">
            <input type="text" name="name" placeholder="Your Name">
            <input type="text" name="phone" placeholder="Your Phone">
            <input type="text" name="date" placeholder="Date">
            <input type="text" name="number" placeholder="Number of people">        
        </div>
        <textarea name="message" cols="30" rows="5" placeholder="Special Requests"></textarea>
        <a class="btn" href="#home">Book a Table <i class="fas fa-angle-right"></i></a>
    </form>
</section>
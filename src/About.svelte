<style>
    #about {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-gap: 3em;
        padding: 5em 18%;
    }
    .text h2 {
        font-size: 1.5rem;
        margin-bottom: 1.25em;
    }
    .text h4 {
        font-size: .8rem;
        line-height: 2;
    }

    .pics {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        place-items: center;
        grid-gap: 5px;
    }
        .pics div img {
            width: 100%;
            object-fit: cover;
        }

    h4 {
        letter-spacing: 3px;
    }

    p {
        line-height: 1.5;
    }

    .text:first-child p {
        margin-bottom: 1em;
    }

    @media only screen and (max-width: 768px) {
        #about {
            grid-template-columns: repeat(1, 1fr);
            grid-gap: 1.5em;
            padding: 3em 10%;
        }
        .text h2 {
            letter-spacing: 5px;
        }
        .text h2 {
            font-size: 1.75rem;
        }
        .text h2 {
            font-size: 1.25rem;
        }
    }
</style>

<!-- Mark Up -->
<section id="about">
    <div class="text">
        <h2>We are Vincent</h2>
        <h4>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem quo rerum explicabo placeat iste deleniti. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quae, sunt.</h4>
        <hr>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia maiores quibusdam beatae optio aliquid nemo delectus velit nam nobis eum illo ipsam, rerum consequatur quo!</p>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolores saepe, sequi molestiae consectetur reiciendis veniam tempore id sint perspiciatis officia commodi ex harum rerum dignissimos consequatur quas laboriosam nam exercitationem excepturi animi repellat libero amet illo totam. Saepe aliquid, sint officia dolorum accusantium numquam error eum, est eveniet, atque dolore.</p>
    </div>

    <div class="pics">
        <div>
            <img src="img/section/about-1.jpg" alt="Photo at Vincents">
        </div>
        <div>
            <img src="img/section/about-2.jpg" alt="Photo at Vincents">
        </div>
    </div>
</section>
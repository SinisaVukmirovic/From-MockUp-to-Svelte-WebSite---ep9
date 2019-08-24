<script>
    const gallery = [
        { img: 'img/gallery/gallery-1.jpg' },
        { img: 'img/gallery/gallery-3.jpg' },
        { img: 'img/gallery/gallery-2.jpg' },
        { img: 'img/gallery/gallery-4.jpg' },
        { img: 'img/gallery/gallery-5.jpg' },
        { img: 'img/gallery/gallery-2.jpg' },
        { img: 'img/gallery/gallery-7.jpg' },
        { img: 'img/gallery/gallery-6.jpg' }
    ];
</script>

<style>
    #gallery {
        padding: 5em 5%;
    }
        #gallery h2 {
            text-align: center;
        }

    .gallery {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(15rem, 1fr));
        grid-gap: 3em;
        margin-top: 2em;
    }
        .gallery div {
            background-color: var(--theme-clr);
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            transition: all 250ms;
        }
            .gallery div::before {
                content: '+';
                position: absolute;
                display: flex;
                justify-content: center;
                align-items: center;
                font-size: 2rem;
                font-weight: lighter;
                width: 3rem;
                height: 3rem;
                border-radius: 50%;
                background-color: var(--bg-clr);
                color: var(--theme-clr);
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                cursor: pointer;
                opacity: 0;
                transition: opacity 250ms;
                z-index: 111;
            }
                .gallery div:hover::before {opacity: 1}
                .gallery div:hover img {opacity: .3}

        .gallery img {
            width: 100%;
            object-fit: cover;
            position: relative;
            background-color: var(--theme-clr);
            cursor: pointer;
            transition: opacity 250ms;
        }

    @media only screen and (max-width: 768px) {
        #gallery {
            padding: 2em 5%;
        }
        .gallery {
            grid-template-columns: repeat(auto-fill, minmax(8rem, 1fr));
            grid-gap: 1em;
            margin-top: 2em;
        }
    }

    @media only screen and (max-height: 414px) {
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(10rem, 1fr));
            grid-gap: 3em;
            margin-top: 2em;
        }
    }
</style>

<!-- Mock Up -->
<section id="gallery">
    <h2>Image gallery</h2>
    <div class="gallery">
    {#each gallery as { img }}
    <div>
        <img src="{img}" alt="Gallery Image">
    </div>
    {/each}
    </div>
</section>
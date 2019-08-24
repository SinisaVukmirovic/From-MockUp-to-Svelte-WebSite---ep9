<script>
    const menus = [
        {
            img: 'img/section/menu-1.jpg',

            menu: [
                {
                    name: 'Margherita',
                    price: '$19.99',
                    info: 'Classic marinara sause, authentic old-world pepperoni'
                },
                {
                    name: 'Tonno al carciofi',
                    price: '$22.99',
                    info: 'Red onions, basil, capers, olives, tuna'
                },
                {
                    name: 'Quatro Formaggi',
                    price: '$18.99',
                    info: 'Gorgonzola, ricotta, mozzarella, taleggio'
                },
                {
                    name: 'Pachino picante',
                    price: '$17.99',
                    info: 'Marrinated cherry tomatoes'
                },
                {
                    name: 'Salmon e pesto di noci',
                    price: '$24.99',
                    info: 'Salmon, walnut pesto'
                },
                {
                    name: 'Pepperoni',
                    price: '$18.99',
                    info: 'Lots of peperoni & mozzarella'
                },
                {
                    name: 'Pomodori panceta',
                    price: '$15.99',
                    info: 'Tomatoes, bacon, onion'
                },
                {
                    name: 'Diabolo',
                    price: '$13.99',
                    info: 'Baby spinach, smoked ham, olives, mozzarella, ect'
                }
            ]
        },
        {
            img: 'img/section/menu-2.jpg',

            menu: [
                {
                    name: 'Margherita',
                    price: '$19.99',
                    info: 'Classic marinara sause, authentic old-world pepperoni'
                },
                {
                    name: 'Tonno al carciofi',
                    price: '$22.99',
                    info: 'Red onions, basil, capers, olives, tuna'
                },
                {
                    name: 'Quatro Formaggi',
                    price: '$18.99',
                    info: 'Gorgonzola, ricotta, mozzarella, taleggio'
                },
                {
                    name: 'Pachino picante',
                    price: '$17.99',
                    info: 'Marrinated cherry tomatoes'
                },
                {
                    name: 'Salmon e pesto di noci',
                    price: '$24.99',
                    info: 'Salmon, walnut pesto'
                },
                {
                    name: 'Pepperoni',
                    price: '$18.99',
                    info: 'Lots of peperoni & mozzarella'
                },
                {
                    name: 'Pomodori panceta',
                    price: '$15.99',
                    info: 'Tomatoes, bacon, onion'
                },
                {
                    name: 'Diabolo',
                    price: '$13.99',
                    info: 'Baby spinach, smoked ham, olives, mozzarella, ect'
                }
            ]
        },
        {
            img: 'img/section/menu-3.jpg',
            
            menu: [
                {
                    name: 'Margherita',
                    price: '$19.99',
                    info: 'Classic marinara sause, authentic old-world pepperoni'
                },
                {
                    name: 'Tonno al carciofi',
                    price: '$22.99',
                    info: 'Red onions, basil, capers, olives, tuna'
                },
                {
                    name: 'Quatro Formaggi',
                    price: '$18.99',
                    info: 'Gorgonzola, ricotta, mozzarella, taleggio'
                },
                {
                    name: 'Pachino picante',
                    price: '$17.99',
                    info: 'Marrinated cherry tomatoes'
                },
                {
                    name: 'Salmon e pesto di noci',
                    price: '$24.99',
                    info: 'Salmon, walnut pesto'
                },
                {
                    name: 'Pepperoni',
                    price: '$18.99',
                    info: 'Lots of peperoni & mozzarella'
                },
                {
                    name: 'Pomodori panceta',
                    price: '$15.99',
                    info: 'Tomatoes, bacon, onion'
                },
                {
                    name: 'Diabolo',
                    price: '$13.99',
                    info: 'Baby spinach, smoked ham, olives, mozzarella, ect'
                }
            ]
        }
    ];
</script>

<style>
    #menu {
        padding: 5em 5%;
    }

    .content {
        text-align: center;
    }
        .content h2 {
            margin-top: .5em;
        }
        .content hr {
            margin: 2em auto;
        }
        .content p {
            max-width: 50%;
            margin: 0 auto;
        }

    .panel {
        display: grid;
        grid-template-columns: 2fr 3fr;
        margin-top: 3em;
    }

    .panel:nth-of-type(2n+1) {
        grid-template-columns: 3fr 2fr;
    }
    .panel:nth-of-type(2n+1) .menu {
        order: 1;
    }
    .panel:nth-of-type(2n+1) div {
        order: 2;
    }
        .panel img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .panel .menu {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            grid-row-gap: 1em;
            grid-column-gap: 3em;
            background-color: var(--menu-bg);
            margin: 1em 0;
            padding: 3em;
        }

            .menu .item {
                cursor: pointer;
                transition: all 250ms;
            }
        
            .menu .item:hover h5 {
                color: var(--theme-clr);
            }

            .menu .item div {
                display: flex;
                justify-content: space-between;
                margin-bottom: .5em;
            }
                .menu .item h5 {
                    font-size: .9rem;
                }
                .menu .item p {
                    font-size: .9rem;
                    color: var(--text-dark);
                }
                .menu .item span {
                    letter-spacing: 3px;
                }

    @media only screen and (max-width: 768px) {
        #menu {
            grid-gap: 1em;
            padding: 2em 10%;
        }
        .content p {
            max-width: 100%;
            margin: 0 auto;
        }
        .panel {
            grid-template-columns: 1fr;
            margin-top: 2em;
        }
            .panel .menu {
                display: grid;
                grid-template-columns: repeat(1, 1fr);
                grid-row-gap: 1em;
                grid-column-gap: 1em;
                background-color: var(--menu-bg);
                margin: 0 1em;
                padding: 1em;
            }
        .menu .item p {
            font-size: .8rem;
        }
        .menu .item span {
            font-size: .8rem;
            letter-spacing: 3px;
        }
        .panel:nth-of-type(2n+1) {
            grid-template-columns: 1fr;
        }
        .panel:nth-of-type(2n+1) .menu {
            order: 2;
        }
        .panel:nth-of-type(2n+1) div {
            order: 1;
        }
    }
</style>

<!-- Mark Up -->
<section id="menu">
    <div class="content">
        <h5>Not just a pizza, but lifestyle</h5>
        <h2>Our Best Offers</h2>
        <hr>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus inventore possimus ea laboriosam rerum, vitae ducimus eum suscipit eos sapiente?</p>
    </div>
    
    {#each menus as { img, menu }}
    <div class="panel">
        <div>
            <img src="{img}" alt="Menu Image">
        </div>
        <div class="menu">
        {#each menu as { name, price, info }}
            <div class="item">
                <div>
                    <h5>{name}</h5> <span>{price}</span>                    
                </div>
                <p>{info}</p>
            </div>
        {/each}
        </div>
    </div>
    {/each}
</section>
<script>
    const stats = [
        {
            number: 138,
            title: 'Menu Items'
        },
        {
            number: '300+',
            title: 'Visitors Everyday'
        },
        {
            number: 12,
            title: 'Years of Experience'
        }
    ];
</script>

<style>
    .numbers {
        padding: 4.5em 18%;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        justify-items: center;
        background-image: url('img/pattern.jpg');
        background-size: cover;
        color: var(--bg-clr);
        text-align: center;
        position: relative;
    }
        .numbers h3 {
            margin-bottom: 1.25em;
        }

    .numbers::after{
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
    
    @media only screen and (max-width: 768px) {
        .numbers {
            padding: 3em 10%;
            grid-template-columns: repeat(1, 1fr);
        }
        .number {
            margin: .75em 0;
        }
        .numbers h3 {
            margin-bottom: .25em;
        } 
    }
</style>

<!-- Mark Up -->
<div class="numbers">
    {#each stats as { number, title }}
        <div class="number">
            <h3>{number}</h3>
            <h4>{title}</h4>
        </div>
    {/each}
</div>
<script>
    
    let films = [
        {id:1, name: 'The god father', year: 1972, genre: 'Crime, Drama', rating: 9.2, image: 'https://pictures-tanzania.jijistatic.com/3341817_MTA4MC0xMzUwLTk0NGZjNzUxMGM.webp'},
        {id:2, name: 'The Shawshank Redemption', year: 1994, genre: 'Drama', rating: 9.3, image: 'https://pictures-tanzania.jijistatic.com/3341817_MTA4MC0xMzUwLTk0NGZjNzUxMGM.webp'},
        {id:3, name: 'The Dark Knight', year: 2008, genre: 'Action, Crime, Drama', rating: 9.0, image: 'https://pictures-tanzania.jijistatic.com/3341817_MTA4MC0xMzUwLTk0NGZjNzUxMGM.webp'},
        {id:4, name: 'SpiderMan 2', year: 2004, genre: 'Action, Adventure, Sci-Fi', rating: 7.3, image: 'https://pictures-tanzania.jijistatic.com/3341817_MTA4MC0xMzUwLTk0NGZjNzUxMGM.webp'},
    ];

</script>


<ul>
    {#each films as film}
        <li>
            <a href="films/{film.id}">
                <!-- svelte-ignore a11y-img-redundant-alt -->
                <img src={film.image} alt="film image">
                <h2>{film.name}</h2>
                <p>{film.year}</p>
                <p>{film.genre}</p>
                <p>{film.rating}</p>
                
            </a>
        </li>
    {/each}
</ul>


<style>
    ul {
        list-style: none;
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        grid-gap: 1rem;
        grid-template-rows: auto;
    }

    li {
        border: 1px solid #ccc;
        padding: 1rem;
        border-radius: 5px;
    }

    a {
        text-decoration: none;
        color: #333;
    }

    img {
        max-width: 100%;
        max-height: 100%;
        object-fit: cover;
    }

    h2 {
        margin: 0;
        background: #333;
        color: #fff;
        padding: .5rem;
    }
    
</style>














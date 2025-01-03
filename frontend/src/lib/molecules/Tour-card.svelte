<script>
  let articles = [
    {
      price: "$25,95",
      location: "Amsterdam",
      img: "/assets/premium-cocktailwalk.png",
      title: "Premium Cocktail Walk",
      description: "De Pijp - Jordaan",
      cocktails: "3 cocktails",
    },
    {
      price: "$25,95",
      location: "Amsterdam",
      img: "/assets/premium-cocktailwalk.png",
      title: "Winter Cocktail Walk",
      description: "Centrum",
      cocktails: "3 cocktails",
    },
    {
      price: "$25,95",
      location: "Amsterdam",
      img: "/assets/premium-cocktailwalk.png",
      title: "Matcha Cocktail Walk",
      description: "Dit is de beschrijving van artikel 3.",
      cocktails: "1 cocktail",
    },
    {
      price: "$25,95",
      location: "Rotterdam",
      img: "/assets/premium-cocktailwalk.png",
      title: "Cocktail Walk",
      description: "Dit is de beschrijving van artikel 4.",
      cocktails: "3 cocktails",
    },
    {
      price: "$25,95",
      location: "Rotterdam",
      img: "/assets/premium-cocktailwalk.png",
      title: "Premium Cocktail Walk",
      description: "Dit is de beschrijving van artikel 5.",
      cocktails: "3 cocktails",
    },
  ];
</script>

<section class="articles">
  {#each articles as article}
    <article>
      <div class="card-header">
        <p>
          <svg
            class="location"
            width="16"
            height="16"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M12 22C11.7667 22 11.5667 21.9333 11.4 21.8C11.2333 21.6667 11.1083 21.4917 11.025 21.275C10.7083 20.3417 10.3083 19.4667 9.825 18.65C9.35833 17.8333 8.7 16.875 7.85 15.775C7 14.675 6.30833 13.625 5.775 12.625C5.25833 11.625 5 10.4167 5 9C5 7.05 5.675 5.4 7.025 4.05C8.39167 2.68333 10.05 2 12 2C13.95 2 15.6 2.68333 16.95 4.05C18.3167 5.4 19 7.05 19 9C19 10.5167 18.7083 11.7833 18.125 12.8C17.5583 13.8 16.9 14.7917 16.15 15.775C15.25 16.975 14.5667 17.975 14.1 18.775C13.65 19.5583 13.275 20.3917 12.975 21.275C12.8917 21.5083 12.7583 21.6917 12.575 21.825C12.4083 21.9417 12.2167 22 12 22ZM12 11.5C12.7 11.5 13.2917 11.2583 13.775 10.775C14.2583 10.2917 14.5 9.7 14.5 9C14.5 8.3 14.2583 7.70833 13.775 7.225C13.2917 6.74167 12.7 6.5 12 6.5C11.3 6.5 10.7083 6.74167 10.225 7.225C9.74167 7.70833 9.5 8.3 9.5 9C9.5 9.7 9.74167 10.2917 10.225 10.775C10.7083 11.2583 11.3 11.5 12 11.5Z"
              fill="#1D1B20"
            />
          </svg>
          {article.location}
        </p>
        <p class="cocktail-price">{article.price}</p>
      </div>
      <img src={article.img} alt={article.title} />
      <h2>{article.title}</h2>
      <div class="card-description">
        <p>{article.description}</p>
        <p>{article.cocktails}</p>
      </div>

      <div class="card-buttons">
        <button class="booking-button">
          Boek nu
          <span
            ><svg
              width="14"
              height="14"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M2.3999 1.99272C1.84762 1.99272 1.3999 2.44044 1.3999 2.99272C1.3999 3.54501 1.84762 3.99272 2.3999 3.99272V1.99272ZM4.69244 2.99272L5.65767 2.73131C5.53961 2.2954 5.14405 1.99272 4.69244 1.99272V2.99272ZM8.41781 16.7479L7.45259 17.0094C7.58285 17.4904 8.04737 17.802 8.54185 17.7402L8.41781 16.7479ZM19.8805 15.3151L20.0045 16.3074C20.4292 16.2543 20.773 15.9368 20.8598 15.5177L19.8805 15.3151ZM21.5999 7.00466L22.5792 7.20727C22.6401 6.91275 22.5652 6.60645 22.3753 6.37324C22.1854 6.14002 21.9007 6.00466 21.5999 6.00466V7.00466ZM5.77901 7.00466L4.81378 7.26608L5.77901 7.00466ZM2.3999 3.99272H4.69244V1.99272H2.3999V3.99272ZM8.54185 17.7402L20.0045 16.3074L19.7565 14.3228L8.29378 15.7557L8.54185 17.7402ZM20.8598 15.5177L22.5792 7.20727L20.6206 6.80206L18.9012 15.1125L20.8598 15.5177ZM3.72721 3.25414L4.81378 7.26608L6.74423 6.74325L5.65767 2.73131L3.72721 3.25414ZM4.81378 7.26608L7.45259 17.0094L9.38304 16.4865L6.74423 6.74325L4.81378 7.26608ZM21.5999 6.00466H5.77901V8.00466H21.5999V6.00466ZM10.9999 20.5C10.9999 20.7761 10.776 21 10.4999 21V23C11.8806 23 12.9999 21.8807 12.9999 20.5H10.9999ZM10.4999 21C10.2238 21 9.9999 20.7761 9.9999 20.5H7.9999C7.9999 21.8807 9.11919 23 10.4999 23V21ZM9.9999 20.5C9.9999 20.2239 10.2238 20 10.4999 20V18C9.11919 18 7.9999 19.1193 7.9999 20.5H9.9999ZM10.4999 20C10.776 20 10.9999 20.2239 10.9999 20.5H12.9999C12.9999 19.1193 11.8806 18 10.4999 18V20ZM18.9999 20.5C18.9999 20.7761 18.776 21 18.4999 21V23C19.8806 23 20.9999 21.8807 20.9999 20.5H18.9999ZM18.4999 21C18.2238 21 17.9999 20.7761 17.9999 20.5H15.9999C15.9999 21.8807 17.1192 23 18.4999 23V21ZM17.9999 20.5C17.9999 20.2239 18.2238 20 18.4999 20V18C17.1192 18 15.9999 19.1193 15.9999 20.5H17.9999ZM18.4999 20C18.776 20 18.9999 20.2239 18.9999 20.5H20.9999C20.9999 19.1193 19.8806 18 18.4999 18V20Z"
                fill="#FFE5D9"
              />
            </svg></span
          >
        </button>
        <button class="readmore-button">Lees meer</button>
      </div>
    </article>
  {/each}
</section>

<style>
  .card-header {
    display: flex;
    justify-content: space-between;
    padding: 0.5em;
  }

  .location {
    padding-top: 0.1em;
  }

  .cocktail-price {
    border: 1px solid #3f2b21;
    border-radius: 8px;
    padding: 0.1em;
  }
  .articles {
    margin-top: 2em;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 20px;
  }

  article {
    width: 80%;
    max-width: 350px;
    height: 425px;
    border: 1px solid #ccc;
    /* padding: 15px; */
    border-radius: 8px;
    background-color: #f9f9f9;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    display: flex;
    flex-direction: column;
    overflow: hidden;
  }
  article {
    background-color: #ffe5d9;
  }

  article img {
    background-color: black;
    display: block;
    object-fit: cover;
    width: 350px;
    position: relative;
  }

  h2 {
    padding-left: 0.5em;
    padding-top: 0.2em;
  }

  .card-description {
    padding-left: 0.5em;
  }

  .card-buttons {
    display: flex;
    margin: 1em;
    gap: 2em;
  }

  .card-buttons {
    padding-left: 1.5em;
  }

  button {
    /* min-width: 135px; */
    border: none;
    padding: 0.7em 1.2em 0.7em 1.2em;
    border-radius: 0.4em;
    white-space: no-wrap;
    cursor: pointer;
  }

  .booking-button {
    background: #3f2b21;
    color: #ffe5d9;
    justify-content: center;
  }

  .readmore-button {
    background: none;
    border: 1px solid #3f2b21;
  }

  span {
    padding-left: 0.5em;
  }

  @media screen and (min-width: 768px) {
    .articles {
      flex-direction: row;
      flex-wrap: wrap;
      gap: 20px;
    }

    article {
      flex: 1 1 32%;
      margin-bottom: 20px;
    }
    button {
      padding: 0.7em 2em 0.7em 2em;
    }
  }
</style>

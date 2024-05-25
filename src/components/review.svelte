<script>
    import { onMount } from 'svelte';
    import axios from 'axios';
  
    let reviews = [];
    let placeId = '1s0xabd110baff26d86d:0x5151ee4236e973e1'; // Replace with your Place ID
    let apiKey = 'AIzaSyAZTRI58idHY0K700k6mrgggidqCOkAyl8'; // Replace with your Google Maps API key
  
    async function fetchGoogleReviews() {
      const url = `https://maps.googleapis.com/maps/api/place/details/json?place_id=${placeId}&key=${apiKey}`;
      try {
        const response = await axios.get(url);
        reviews = response.data.result.reviews;
      } catch (error) {
        console.error('Error fetching reviews:', error);
      }
    }
  
    onMount(() => {
      fetchGoogleReviews();
    });
  </script>
  
  <div class="spacing"></div>
<div class="spacing2"></div>

<section id="reviews">
    <div id="reviewsTitle">
      <div id="reviewsText">
  <h1>Google Reviews</h1>
</div>
</div>
  <div>
    {#if reviews.length > 0}
      {#each reviews as review}
        <div class="review">
          <h3>{review.author_name}</h3>
          <p>Rating: {review.rating}</p>
          <p>{review.text}</p>
        </div>
      {/each}
    {:else}
      <p>Loading reviews...</p>
    {/if}
  </div>
</section>
  

  <style>
     .spacing {
    margin-top: 0.5em;
    background-color: #0f75bc;
    height: 2.5em;
    width: 100%;
    grid-column-start: 1;
    grid-column-end: 5;
  }
  .spacing2 {
    height: 0.75em;
  }
  #reviews {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    justify-items: center;
  }

  #reviewsTitle {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    margin-bottom: 2em;
    grid-column-start: 1;
    grid-column-end: 5;
    width: 100%;
    height: 100%;
    align-content: center;
    background-color: #91d1e7;
    border-radius: 15px;
  }
  #reviewsText {
    background-color: white;
    width: 100%;
    text-align: center;
    grid-column-start: 2;
    grid-column-end: 3;
    border-radius: 15px;
  }
    .review {
      border: 1px solid #ccc;
      padding: 10px;
      margin: 10px 0;
    }
  </style>
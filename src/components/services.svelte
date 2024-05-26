<script>
</script>

<div class="spacing"></div>
<div class="spacing2"></div>

<section id="services">
  <div id="servicesTitle">
    <div id="serviceText">
      <h1>Services</h1>
    </div>

  </div>
  

  <section class="cardWithBG" id="hours">
    <div class="headings" id="services"><h2>Hourly:</h2></div>
    <p>$180/hour for 1 dog (40$/hr for additonal dog)</p>
    <p>
      Comprehensive dog training services - covers everything your dog needs to
      reach their full potential
    </p>
    <p>
      - personalized training experience that aligns perfectly with your vision
    </p>
    <p>
      - make a list of your dog's dream attributes- work together to achieve
      them
    </p>
    <p>- obedience basics tobehavioral issues</p>
  </section>

  <section class="cardWithBG" id="packages">
    <div class="headings" id="services"><h2>Packages:</h2></div>
    <p>- For 1 dog</p>
    <p>$1200 for 6 sessions and 2 group classes</p>
    <p>- For 2 dogs</p>
    <p>$1600 for 7 sessions and 3 group classes</p>
    <p>- For 3 dogs</p>
    <p>$2000 for 8 sessions and 4 group classes</p>
  </section>

  <section class="cardWithBG">
    <div class="headings" id="services"><h2>Group Classes:</h2></div>
    <p>$50/family (additional $20/per dog)</p>
    <p>
      Designed to challenge both you and your canine companion with intense
      training sessions amidst high-stimulus distractions, ensuring you are
      prepared for any scenario
    </p>
    <p>- available exclusively to my current clientele</p>
    <p>
      - offer a unique approach to training, ensuring everyone is on the same
      page and has undergone identical training methods
    </p>
    <p>
      - experience the benefits of a supportive community of well-trained dogs
      while your furry friend engages in obedience training and controlled play
      sessions
    </p>
    <p>- all in a safe and structured environment</p>
    <p>
      - high quality single ingredient dog treats and cold water are always
      provided
    </p>
    <p>- class locations and times vary</p>
  </section>
  <section class="cardWithBG">
    <div class="headings" id="services"><h2>Board and Train:</h2></div>
    <p>Intensive In-Home Training for dog clients to reside with me</p>
    <p>
      - receive personalized one-on-one sessions morning and evening, each
      lasting a minimum of an hour
    </p>
    <p>- tailored to your dog's needs</p>
    <p>- experience pack training alongside our expert demo dogs!</p>
    <p>
      - duration and intensity of the program vary based on the number of weeks
      boarded and the specific behavioral needs of your furry friend
    </p>
    <p>
      - pricing can be discussed through an in person FREE consultation or via
      phone call
    </p>
    <p>- Limited Spots Available!</p>
  </section>
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
  .headings {
    margin-top: 1em;
    height: 2.5em;
    grid-column-start: 1;
    grid-column-end: 5;
  }

  .headings > * {
    /* styles for child elements of class headings */
    background-color: white;
    padding: 0.5em;
    border-radius: 15px;
    border: solid 5px #112b5e;
    text-align: center;
    margin-top: -0.5em;
  }
  #services {
    display: grid;
    justify-items: center;
    margin-bottom: 2em;
  }

  #servicesTitle {
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
  #serviceText {
    background-color: white;
    width: 100%;
    text-align: center;
    grid-column-start: 2;
    grid-column-end: 3;
    border-radius: 15px;
  }
  .svgCard {
    width: 100%;
    height: 100%;
  }
  .card {
    z-index: -1;
  }
  .cardWithBG {
    width: 100%;
    height: 100%;
    background-image: url("../img/blueGrad.svg");

    background-repeat: no-repeat;
    background-size: cover;
    z-index: -1;
  }
  .cardWithBG > * {
    padding: 0.5em;
    border-radius: 15px;
    margin: 1em;
  }

  #packages {
    background-image: url("../img/hours.jpg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  @media (max-width: 800px) {
    #services {
      display: inline;
    }
  }
</style>

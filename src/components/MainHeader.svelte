<header class="header">
  <div class="hashtag">
</div>
  <nav>
    <ul class="centered-links">
      <li><a href="#">Home</a></li>
      <li><a href="#aboutme">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#contact">Contact</a></li>
      <li><a href="#reviews">Reviews</a></li>
    </ul>
  </nav>
</header>


<style>
    header {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        display: grid;
        grid-template-columns: 10% 90%;
        /* background-color: #f1c2ac; */
        border-radius: 5px;
        max-height: 3em;
    }

    .headerLogo {
        /* position: fixed; */
        width: 75%;
        /* height:100%;
                justify-self: center; */
        /* background-color: #f1c2ac; */
        /* border-radius: 15px; */
        /* margin-left: -1%; */
    }

    .hashtag {
        width: 100%;
        height: 100%;
        background-color: white;
        text-align: center;
        align-content: center;
        font-weight: 800;
        font-size: 1.75em;
        background-image: url("../img/ckcLogoBadge.png");
        background-position: center;
        background-repeat: no-repeat;
        background-size:contain;
    }

    nav {
        background-color: #112b5e;
        width: 100%;
        text-align: center;
        align-content: center;

    }

    ul {
        list-style-type: none;
        display: grid;
        /* align-items: center; */
        grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
        width: 100%;
        height: 100%;
        padding: 0;
        margin: 0;
        /* justify-self: center;
                margin-left: -2%; */
    }

    li {
        /* background-color: #25aae1; */
        padding: 10px 20px;
        margin: 1em;
        border-radius: 5px;
        
        
    }
    a:hover {
        background-color: #0f75bc;
        padding: 1em;
        border-radius: 15px;
        font-weight: 800;
        font: 1.5em sans-serif;
    }
    a {
        text-decoration: none;
        color: white;
        font-weight: 800;
        font: 1.5em sans-serif;
    }

    /* Media Query for Mobile View */
    @media (max-width: 800px) {
        header {
            position: absolute;
            grid-template-columns: 100%;
            height: 320px;
        }
        .headerLogo {
            width: 100%;
        }
        .hashtag {
            margin-left: 80px;
            margin-top: 80px;
            height: 150px;
            width: 150px;
            position: absolute;
            font-size: 1.5em;
            border-radius: 50%;
        }
        ul {
            grid-template-columns: 1fr;
        }
        li {
            margin: 0.5em;
        }
    }
    @media (max-width: 640px) {
        .hashtag{
            margin-left: 20px;
            margin-top: 20px;
            height: 100px;
            width: 100px;
        }
    }
</style>

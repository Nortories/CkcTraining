<script>
import { onMount } from 'svelte';

onMount(() => {
    const form = document.getElementById('contactForm');
    form.addEventListener('submit', handleSubmit);
});

function handleSubmit(event) {
    event.preventDefault();

    const formData = new FormData(event.target);
    const name = formData.get('name');
    const email = formData.get('email');
    const message = formData.get('message');

    const emailData = {
        name,
        email,
        message
    };

    // Send email using your preferred method (e.g. fetch, axios, etc.)
    // Example using fetch:
    fetch('/api/send-email', {
        method: 'POST',
        headers: {
            'Content-Type': 'application/json'
        },
        body: JSON.stringify(emailData)
    })
        .then(response => response.json())
        .then(data => {
            console.log('Email sent successfully:', data);
            // Optionally show a success message to the user
        })
        .catch(error => {
            console.error('Error sending email:', error);
            // Optionally show an error message to the user
        });
}
</script>

<div class="spacing"></div>
<div class="spacing2"></div>

<section id="contact">
  <div id="contactTitle">
    <div id="contactText">
      <h1>Contact</h1>
    </div>
  </div>
<form id="contactForm">
    <div class="form-group">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required>
    </div>
    <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
    </div>
    <div class="form-group">
        <label for="message">Message:</label>
        <textarea id="message" name="message" required></textarea>
    </div>
    <button type="submit">Submit</button>
</form>
<section>
    <div id="contactInfo">
        <h2>Chantel Clark</h2>
        <p>Dog Trainer</p>
        <p>Southern Utah</p>
        <p>Phone: 435-525-3493</p>
        <p>Email: Ck9ctraining@gmail.com</p>
        <br>
        <p>Social media:</p>
        <p><a href="https://www.instagram.com/ckctraining/"><img src="/img/instagram.png" alt="Instagram" width="24" height="24"> @ckctraining</a></p>
        <p><a href="https://www.facebook.com/CKCtraining/"><img src="/img/facebook.png" alt="Facebook" width="24" height="24"> @ckctraining</a></p>
        <p><a href="https://www.tiktok.com/@ckctraining"><img src="/img/tiktok.png" alt="TikTok" width="24" height="24"> @ckctraining</a></p>
    </div>
</section>
</section>

<style>
    #contactForm {
        display: grid;
        grid-template-columns: 1fr;
        gap: 1em;
        margin: 1em;
        padding: 1em;
        background-color: #f5f5f5;
        border-radius: 5px;
        width: 100%;
    }

    .form-group {
        display: grid;
        gap: 0.5em;
        padding-right: 1em;
    }

    label {
        font-weight: bold;
    }

    input,
    textarea {
        width: 100%;
        padding: 0.5em;
        border: 1px solid #ccc;
        border-radius: 3px;
    }

    button[type="submit"] {
        padding: 0.5em 1em;
        background-color: antiquewhite;
        color: black;
        border: solid 1px;
        border-radius: 3px;
        cursor: pointer;
    }
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

  #contact {
    display: grid;
    grid-template-columns: 1fr 1fr;
    justify-items: center;
  }
  #contactTitle {
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
  #contactText {
    background-color: white;
    width: 100%;
    text-align: center;
    grid-column-start: 2;
    grid-column-end: 3;
    border-radius: 15px;
  }

</style>
<script>
    import { createEventDispatcher } from "svelte";
  
    export let title, message;
    
  </script>
  
  <div class="card">
    <h1 class="title">{title}</h1>
    <p>{@html message}</p>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <img
      src="https://cdn-icons-png.flaticon.com/512/9309/9309009.png"
      alt="remove"
      width="24"
    />
  </div>
  
  <style>
    @import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");
    .card {
      position: relative;
      top: 0;
      bottom: 0;
      right: 0;
      left: 0;
      width: fit-content;
      border: 1px solid black;
      padding: 15px 25px;
      margin: 20px;
      border-radius: 10px;
      transition: all 0.3s ease;
      height: fit-content;
    }
    .title {
      font-family: "Lato", sans-serif;
      margin-bottom: 7px;
      text-align: center;
      padding-right: 15px;
      transition: all 0.3s ease;
      color: #1e1e1e;
    }
    p {
      font-family: "Poppins", sans-serif;
      font-weight: 500;
      font-size: 1.2rem;
      color: #3c3c3c;
    }
    img {
      position: absolute;
      right: 5px;
      top: 5px;
      transition: all 0.3s ease;
      opacity: 0;
    }
    .card:hover img {
      opacity: 1;
    }
    .card:hover p {
      color: #000000;
    }
    .card:hover h1 {
      transition: all 0.3s ease;
  
      color: rgb(0, 89, 255);
    }
    @media only screen and (min-device-width: 320px) and (max-device-width: 480px) {
      /* Styles */
      .card {
        width: 200px;
      }
    }
  </style>
  
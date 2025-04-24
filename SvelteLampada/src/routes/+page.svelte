<script>
    let isOn = false;
  
    function toggleLight() {
      isOn = !isOn;
    }
  </script>
  
  <style>
    main {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
  
      text-align: center;
      padding: 20px;
      background-color: black;
      color: white;
      transition: background-color 2s;
      min-height: 100vh;
    }
  
    .light-on {
      background-color: #f1f17e;
      color: black;
    }
  
    button {
        margin-top: 20px;
        padding: 15px 30px;
        font-size: 18px;
        font-weight: bold;
        cursor: pointer;
        border: none;
        border-radius: 8px;
        background-color: #0c3b5d;
        color: #000;
        transition: background-color 0.3s, transform 0.2s;
    }

    button:hover {
        background-color: #105897;
        transform: scale(1.05);
    }

    button:active {
        transform: scale(0.98);
    }

  
    img {
      width: 150px;
      display: block;
      margin: 0 auto;
    }
  </style>
  
  
  <main class:light-on={isOn}>
    <div>
      <img
        src={isOn
          ? "https://i.postimg.cc/6QyTynzr/bulb-on.png"
          : "https://i.postimg.cc/KjK1wL3c/bulb-off.png"}
        alt="Lâmpada"
      />
      <br />
      <button on:click={toggleLight}>
        {isOn ? "Apagar" : "Acender"}
      </button>
    </div>
  </main>
  
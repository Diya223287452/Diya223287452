<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Vue 3 Concepts Experimentation</title>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz@10..48&display=swap"
      rel="stylesheet"
    />
    <script src="https://cdn.jsdelivr.net/npm/vue@3.2.20/dist/vue.global.js"></script>
    <style>
      body {
        font-family: Bricolage Grotesque;
        margin: 0;
        padding: 0;
        background-color: #f5f5f5;
      }

      #app {
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 700px;
      }

      .section {
        background-color: #fff;
        padding: 30px;
        border-radius: 10px;
        box-shadow: 0px 6px 20px rgba(135, 59, 59, 0.1);
        margin: 10px;
        margin-left: 40px;
        transform: translateY(0);
        transition: transform 0.5s cubic-bezier(0.15, 1, 0.2, 2),
          box-shadow 0.15s ease-in-out;
      }

      .section:hover {
        transform: translateY(-17px);
        box-shadow: 0px 10px 30px rgba(58, 50, 50, 0.2);
      }

      h1 {
        text-align: center;
        margin-bottom: 35px;
        color: #45bdbd;
        font-size: 36px;
        font-style: Tulpen One;
        text-shadow: 3px 3px 5px rgba(98, 197, 239, 0.1);
      }

      .conditional-content {
        margin: 15px;
        font-size: 10px;
        opacity: 0;
        transform: translateY(30px);
        transition: opacity 0.7s cubic-bezier(0.19, 1, 0.22, 1),
          transform 0.7s cubic-bezier(0.19, 1, 0.22, 1);
      }

      .fade-in {
        opacity: 0.15;
        transform: translateY(0);
      }

      .toggle-content {
        color: #6e8aa7;
        cursor: default;
        transition: color 0.3s ease-in-out;
      }

      .toggle-content:hover {
        color: #455463;
      }

      .toggle-info {
        margin: 10px 0;
        opacity: 0;
        transform: translateY(20px);
        transition: opacity 0.7s cubic-bezier(0.19, 1, 0.22, 1),
          transform 0.7s cubic-bezier(0.19, 1, 0.22, 1);
      }

      .visible {
        opacity: 1;
        transform: translateY(0);
      }

      ul {
        list-style: circle;
        margin: 15px 0;
        padding-left: 30px;
      }

      .list-item {
        margin-bottom: 10px;
        opacity: 0;
        transform: translateX(-30px);
        transition: opacity 0.7s cubic-bezier(0.19, 1, 0.22, 1),
          transform 0.7s cubic-bezier(0.19, 1, 0.22, 1);
      }

      .list-item.fade-in {
        opacity: 1;
        transform: translateX(0);
      }

      .nested-content {
        margin-top: 30px;
      }

      .input-field {
        padding: 10px;
        border: 2px solid #695e5e;
        border-radius: 8px;
        font-size: 18px;
        width: 100%;
        margin-bottom: 15px;
        transition: border-color 0.5s cubic-bezier(0.19, 1, 0.22, 1);
      }

      .input-field:focus {
        border-color: #395c83;
      }

      .typed-text {
        font-size: 20px;
        color: #395c83;
        opacity: 0;
        transform: scale(0.95);
        transition: opacity 0.7s cubic-bezier(0.19, 1, 0.22, 1),
          transform 0.15s cubic-bezier(0.19, 1, 0.22, 1);
      }

      .typed-visible {
        opacity: 1;
        transform: scale(1);
      }
    </style>
  </head>
  <body>
    <div id="app">
      <button @click="awesome = !awesome">Toggle</button>
      <h1 v-if="awesome">Vue 3 Concepts</h1>
      <h1 v-else>Oops :|</h1>
      <h2></h2>
      <div class="section"></div>

      <div class="section"></div>
    </div>

    <script src="app.js"></script>
  </body>
</html>

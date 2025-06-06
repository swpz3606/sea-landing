<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>พักใจไว้ที่ทะเล</title>
  <link href="https://fonts.googleapis.com/css2?family=Sriracha&family=Prompt:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Prompt', sans-serif;
      background-color: #ffffff;
      color: #333;
    }

    /* Hero Section */
    .hero {
      height: 100vh;
      background: url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e') no-repeat center center/cover;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: white;
      text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.5);
      padding: 0 20px;
    }

    .hero h1 {
      font-size: 3.5rem;
      font-family: 'Sriracha', cursive;
    }

    .hero p {
      font-size: 1.5rem;
      margin: 20px 0;
    }

    .cta-btn {
      background-color: rgba(255, 255, 255, 0.2);
      border: 2px solid white;
      padding: 12px 30px;
      color: white;
      font-size: 18px;
      border-radius: 30px;
      cursor: pointer;
      transition: 0.3s;
    }

    .cta-btn:hover {
      background-color: white;
      color: #0077be;
    }

    /* Quote Section */
    .quotes {
      padding: 60px 20px;
      text-align: center;
      background-color: #e6f7ff;
    }

    .quotes h2 {
      font-size: 2rem;
      margin-bottom: 20px;
      color: #0077be;
    }

    #quote {
      font-size: 1.5rem;
      color: #333;
      margin-bottom: 30px;
    }

    .change-quote-btn {
      padding: 10px 20px;
      background-color: #0077be;
      color: white;
      border: none;
      font-size: 16px;
      border-radius: 20px;
      cursor: pointer;
    }

    .change-quote-btn:hover {
      background-color: #005f99;
    }

    @media (max-width: 768px) {
      .hero h1 {
        font-size: 2.5rem;
      }

      .hero p {
        font-size: 1.2rem;
      }

      #quote {
        font-size: 1.2rem;
      }
    }
  </style>
</head>
<body>

  <!-- Hero Section -->
  <section class="hero">
    <h1>พักใจไว้ที่ทะเล</h1>
    <p>ถ้าใจคุณล้า... ทะเลจะช่วยเยียวยาเอง</p>
    <button class="cta-btn" onclick="scrollToQuotes()">ไปดูแคปชั่นทะเล</button>
  </section>

  <!-- Quotes Section -->
  <section class="quotes" id="quotes-section">
    <h2>แคปชั่นทะเลวันนี้ 🌴</h2>
    <div id="quote">"ทะเลไม่เคยเปลี่ยน... แต่ใจคนเปลี่ยนตลอดเวลา"</div>
    <button class="change-quote-btn" onclick="changeQuote()">เปลี่ยนแคปชั่น</button>
  </section>

  <script>
    const quotes = [
      "ทะเลเรียกหา ใจก็จะพาไป",
      "พายุคลื่นยังสงบได้ ใจเราก็เช่นกัน",
      "ทะเลไม่เคยหายไป… แค่รอให้ใจเราว่างพอจะกลับไปหา",
      "ถ้าใจมันเซ ไปทะเลก็ยังดีกว่าอยู่เฉย ๆ",
      "อยากให้ใจนิ่งเหมือนทะเลในวันที่ไม่มีคลื่น"
    ];

    function changeQuote() {
      const randomIndex = Math.floor(Math.random() * quotes.length);
      document.getElementById('quote').textContent = quotes[randomIndex];
    }

    function scrollToQuotes() {
      document.getElementById('quotes-section').scrollIntoView({ behavior: 'smooth' });
    }
  </script>

</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ebb+Tress | Sign Up for Full Hair Emergency Guide</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Lato:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Lato', sans-serif;
      background-color: #ffffff;
      color: #185228;
      margin: 0;
      padding: 20px;
      line-height: 1.6;
      text-align: center;
    }
    .container {
      max-width: 600px;
      margin: 0 auto;
      padding: 20px;
    }
    h1 {
      font-family: 'Playfair Display', serif;
      font-size: 28px;
      color: #185228;
      margin-bottom: 20px;
      line-height: 0.3;
    }
    p {
      text-align: center;
    }
    .form-group {
      margin-bottom: 15px;
    }
    label {
      font-size: 16px;
      display: block;
      margin-bottom: 5px;
    }
    input[type="text"],
    input[type="email"] {
      width: 100%;
      max-width: 300px;
      padding: 10px;
      font-size: 16px;
      border: 1px solid #D4AF37;
      border-radius: 5px;
    }
    button {
      font-family: 'Lato', sans-serif;
      font-size: 16px;
      padding: 10px 20px;
      background-color: #185228;
      color: #ffffff;
      border: none;
      cursor: pointer;
      border-radius: 5px;
    }
    button:hover {
      background-color: #D4AF37;
      color: #185228;
    }
    #success-message {
      display: none;
      margin-top: 20px;
      padding: 15px;
      background-color: #185228;
      color: #ffffff;
      border-radius: 5px;
    }
    #error-message {
      display: none;
      margin-top: 20px;
      padding: 15px;
      background-color: #ffcccc;
      color: #185228;
      border-radius: 5px;
    }
    .footer {
      font-size: 12px;
      text-align: center;
      margin-top: 20px;
      color: #666;
    }
    @media (max-width: 600px) {
      h1 { font-size: 24px; }
      label { font-size: 14px; }
      button { font-size: 14px; }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Ebb+Tress</h1>
    <h1>Sign Up for Your Full Hair Emergency Guide</h1>
    <p>Unlock deeper solutions for only $10! Enter your details to proceed.</p>

    <form id="signup-form">
      <div class="form-group">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required>
      </div>
      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
      </div>
      <button type="submit">Proceed to Payment ($10)</button>
    </form>

    <div id="success-message">
      <p>Thank you! Please complete your $10 payment below to receive your Full Hair Emergency Guide via email:<br>
        <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
          <input type="hidden" name="cmd" value="_xclick">
          <input type="hidden" name="business" value="ebbandtress@gmail.com">
          <input type="hidden" name="item_name" value="Full Hair Emergency Guide">
          <input type="hidden" name="amount" value="10.00">
          <input type="hidden" name="currency_code" value="USD">
          <input type="hidden" name="return" value="https://ebbtress.github.io/thank-you">
          <input type="hidden" name="cancel_return" value="https://ebbtress.github.io">
          <input type="image" src="https://www.paypalobjects.com/en_US/i/btn/btn_buynow_LG.gif" border="0" name="submit" alt="PayPal - The safer, easier way to pay online!">
        </form>
      </p>
    </div>
    <div id="error-message">
      <p>There was an error processing your request. Please try again later or contact support at ebbandtress@gmail.com.</p>
    </div>

    <div class="footer">© 2025 Ebb+Tress | You Deserve Healthy Hair!</div>
  </div>

  <script>
    document.getElementById('signup-form').addEventListener('submit', async function(event) {
      event.preventDefault();
      
      const name = document.getElementById('name').value;
      const email = document.getElementById('email').value;
      const data = { name, email, product: 'Full Hair Emergency Guide' };

      try {
        const response = await fetch('https://script.google.com/macros/s/AKfycbyHNbt_5SvckdWPAfrVEXe3pyHtKWeGRtpni0SMYjHuH3L0E-fOAHHeLQxrYKHCDIAYnQ/exec', {
          method: 'POST',
          body: JSON.stringify(data),
          headers: { 'Content-Type': 'application/json' },
          mode: 'no-cors'
        });
        document.getElementById('signup-form').style.display = 'none';
        document.getElementById('success-message').style.display = 'block';
      } catch (error) {
        document.getElementById('error-message').style.display = 'block';
        console.error('Fetch error:', error);
      }
    });
  </script>
</body>
</html># ebbandtress-fullguidesignup

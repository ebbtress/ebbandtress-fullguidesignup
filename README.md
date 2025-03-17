<!DOCTYPE html>
<html>
<body>
  <form id="testForm">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" value="Cheyenne"><br>
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" value="cheyenne@example.com"><br>
    <label for="product">Product:</label>
    <select id="product" name="product">
      <option value="Free Hair Emergency Guide">Free Hair Emergency Guide</option>
      <option value="Full Hair Emergency Guide">Full Hair Emergency Guide</option>
    </select><br>
    <button type="submit">Submit</button>
  </form>
  <div id="response"></div>

  <script>
    document.getElementById('testForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const name = document.getElementById('name').value;
      const email = document.getElementById('email').value;
      const product = document.getElementById('product').value;
      const params = `name=${encodeURIComponent(name)}&email=${encodeURIComponent(email)}&product=${encodeURIComponent(product)}`;
      fetch('https://script.google.com/macros/s/AKfycbzUaqgqIplkGliQsuWrCFiHdSdtgXy7vUjjVRa2dPf6jjiGtafK2LSU0r6mrYYqcqCY/exec', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/x-www-form-urlencoded'
        },
        body: params
      })
      .then(response => response.text())
      .then(data => {
        document.getElementById('response').innerText = 'Response: ' + data;
      })
      .catch(error => {
        document.getElementById('response').innerText = 'Error: ' + error;
      });
    });
  </script>
</body>
</html>

# T-i-x-u
<!DOCTYPE html>
<html>
<head>
  <title>Tài Xỉu</title>
</head>
<body>
  <h1>Game Tài Xỉu</h1>

  <button onclick="play('tai')">Chọn Tài</button>
  <button onclick="play('xiu')">Chọn Xỉu</button>

  <h2 id="result"></h2>

  <script>
    function rollDice() {
      return Math.floor(Math.random() * 6) + 1;
    }

    function play(choice) {
      let d1 = rollDice();
      let d2 = rollDice();
      let d3 = rollDice();

      let total = d1 + d2 + d3;

      let ketqua = total >= 11 ? 'tai' : 'xiu';

      let text = `Xúc xắc: ${d1}, ${d2}, ${d3} → Tổng: ${total} → `;

      if (choice === ketqua) {
        text += "Bạn thắng!";
      } else {
        text += "Bạn thua!";
      }

      document.getElementById("result").innerText = text;
    }
  </script>
</body>
</html>

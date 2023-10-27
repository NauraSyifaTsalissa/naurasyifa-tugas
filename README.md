<html>
<head>
<meta charset="utf-8">
<style>
.kalk(margin: 40%;>
.kalk .butt{magrin:2px;48px;height:25px;font-weight:bold;}
</style>
</head>
<body>
 <br>
 </TD>
 </TR>
	
<div class="calculator">
        <input type="text" id="display" readonly>
        <br>
        <input type="button" value="1" onclick="addToDisplay('1')">
        <input type="button" value="2" onclick="addToDisplay('2')">
        <input type="button" value="3" onclick="addToDisplay('3')">
        <input type="button" value="+" onclick="addToDisplay('+')">
        <br>
        <input type="button" value="4" onclick="addToDisplay('4')">
        <input type="button" value="5" onclick="addToDisplay('5')">
        <input type="button" value="6" onclick="addToDisplay('6')">
        <input type="button" value="-" onclick="addToDisplay('-')">
        <br>
        <input type="button" value="7" onclick="addToDisplay('7')">
        <input type="button" value="8" onclick="addToDisplay('8')">
        <input type="button" value="9" onclick="addToDisplay('9')">
        <input type="button" value="*" onclick="addToDisplay('*')">
        <br>
        <input type="button" value="C" onclick="clearDisplay()">
        <input type="button" value="0" onclick="addToDisplay('0')">
        <input type="button" value="=" onclick="calculate()">
        <input type="button" value="/" onclick="addToDisplay('/')">
	  <h1>modulusCalculator</h1>
	  <input type="number" id="angka1" placeholder="Masukkan angka kesatu">
        <input type="number" id="angka2" placeholder="Masukkan angka kedua">
        <button onclick="hitungModulus()">Hitung</button>
        <p>Hasil: <span id="hasil"></span></p>
	  <br>
 <script>
        function hitungModulus() {
            var angka1 = parseFloat(document.getElementById("angka1").value);
            var angka2 = parseFloat(document.getElementById("angka2").value);

            if (!isNaN(angka1) && !isNaN(angka2)) {
                var hasil = angka1 % angka2;
                document.getElementById("hasil").textContent = hasil;
            } else {
                document.getElementById("hasil").textContent = "Masukkan angka yang valid";
            }
        }
    </script>
  <script>
        function addToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function calculate() {
            try {
                document.getElementById('display').value = eval(document.getElementById('display').value);
            } catch (error) {
                document.getElementById('display').value = 'Error';
            }
        }
    </script>

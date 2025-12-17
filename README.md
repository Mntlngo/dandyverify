# dandyverify









<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Dandy Hats | Verify</title>
<style>
body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
  background: white;
  text-align: center;
  color: black;
}

.container {
  max-width: 400px;
  margin: auto;
  padding: 40px 20px;
}

.logo {
  font-size: 28px;
  font-weight: bold;
}

.sub {
  font-size: 14px;
  letter-spacing: 2px;
  margin-bottom: 30px;
}

.cap-img {
  width: 100%;
  margin: 30px 0;
}

.scan-text {
  font-size: 14px;
  letter-spacing: 2px;
}

.scan-count {
  font-size: 32px;
  font-weight: bold;
  margin-bottom: 30px;
}

.verify-btn {
  background: black;
  color: white;
  border: none;
  padding: 18px 40px;
  font-size: 20px;
  border-radius: 30px;
  cursor: pointer;
}
</style>
</head>

<body>
  <div class="container">

    <div class="logo">AUTHENTIC</div>
    <div class="sub">DANDY x TOMBOCHIO</div>

    <img src="dandy-tombochio.jfif" class="cap-img" alt="Dandy Hat">

    <div class="scan-text">TOTAL SCAN COUNT :</div>
    <div class="scan-count" id="scanCount">0 SCANS</div>

    <button class="verify-btn"
      onclick="alert('This Dandy x Tombochio hat is 100% authentic')">
      VERIFY
    </button>

  </div>

<script>
let scans = localStorage.getItem("dandyScans");

if (!scans) {
  scans = 1;
} else {
  scans = parseInt(scans) + 1;
}

localStorage.setItem("dandyScans", scans);
document.getElementById("scanCount").innerText = scans + " SCANS";
</script>

</body>
</html>

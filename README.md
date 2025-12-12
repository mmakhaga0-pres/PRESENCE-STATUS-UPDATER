<!DOCTYPE html>
<html>
<head>
<title>Presence Panel</title>
<style>
button {
  font-size: 28px;
  width: 90%;
  padding: 20px;
  margin: 15px;
  border-radius: 12px;
}
.here { background-color: #2ecc71; }
.not { background-color: #e74c3c; }
.long { background-color: #3498db; }
</style>
</head>
<body>

<h1>Presence Check</h1>

<button class="here" onclick="sendStatus('I am here')">🟢 I am here</button>
<button class="not" onclick="sendStatus('Not here, back later')">🔴 Not here (back later)</button>
<button class="long" onclick="sendStatus('Here for long')">🔵 Here for long</button>

<script>
function sendStatus(stat) {
  fetch("(https://script.google.com/macros/s/AKfycbzEpwaVy8BnWwej9sjFsIgseNTFp-98SIieXJx5d1vE2PQS50kn4i653DuSkJGbj1O5/exec)" + encodeURIComponent(stat))
    .then(r => alert("Status sent: " + stat));
}
</script>

</body>
</html>

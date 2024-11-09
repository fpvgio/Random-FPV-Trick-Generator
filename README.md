<html>
<head>
<style>
body {
  font-family: sans-serif;
  text-align: center;
  min-height: 100vh; /* Ensure full viewport height */
  display: flex;
  flex-direction: column;
  justify-content: center; /* Vertically center content */
  align-items: center; /* Horizontally center content */
  background-color: #f0f0f0;
}

button {
  padding: 15px 30px;
  font-size: 18px;
  background-color: #4CAF50;
  color: white;
  border: none;
  cursor: pointer;
  border-radius: 5px;
}

ul {
  list-style: none;
  padding: 0;
  margin-top: 20px;
}

li {
  margin-bottom: 10px;
}

a {
  text-decoration: none;
  color: #333;
}
</style>
</head>
<body>

<button id="trickButton">Get 5 Tricks</button>

<ul id="trickList"></ul>

<script>
const trickLinks = [
  "https://prowhooper.com/flip",
  "https://prowhooper.com/double-flip",
  "https://prowhooper.com/roll",
  "https://prowhooper.com/double-roll",
  "https://prowhooper.com/yaw-spin",
  "https://prowhooper.com/inverted-rewind",
  "https://prowhooper.com/vanny-roll",
  "https://prowhooper.com/rubiks-cube",
  "https://prowhooper.com/cubiks-rube",
  "https://prowhooper.com/juicy-flick",
  "https://prowhooper.com/snapback",
  "https://prowhooper.com/inverted-yaw-spin",
  "https://prowhooper.com/inverted-yaw-tracking",
  "https://prowhooper.com/powerloop",
  "https://prowhooper.com/immelmann",
  "https://prowhooper.com/power-split",
  "https://prowhooper.com/power-flip",
  "https://prowhooper.com/reversed-power-flip",
  "https://prowhooper.com/power-swap",
  "https://prowhooper.com/power-switch",
  "https://prowhooper.com/power-roll",
  "https://prowhooper.com/loop-to-matty",
  "https://prowhooper.com/inverted-360-powerloop",
  "https://prowhooper.com/barani",
  "https://prowhooper.com/maverick-loop",
  "https://prowhooper.com/mavvy-roll",
  "https://prowhooper.com/half-mavvy",
  "https://prowhooper.com/maviks-loop",
  "https://prowhooper.com/mavani",
  "https://prowhooper.com/donkey-loop",
  "https://prowhooper.com/matty-flip",
  "https://prowhooper.com/matty-twister",
  "https://prowhooper.com/half-matty",
  "https://prowhooper.com/540-half-matty",
  "https://prowhooper.com/matty-360",
  "https://prowhooper.com/forani",
  "https://prowhooper.com/split-s-2",
  "https://prowhooper.com/540-split-s",
  "https://prowhooper.com/splitback",
  "https://prowhooper.com/split-yaw",
  "https://prowhooper.com/split-stall-matty-rewind",
  "https://prowhooper.com/orbits",
  "https://prowhooper.com/cradle",
  "https://prowhooper.com/side-lock-rewind",
  "https://prowhooper.com/whiplash",
  "https://prowhooper.com/pole-dance",
  "https://prowhooper.com/trippy-spin",
  "https://prowhooper.com/trippy-switch",
  "https://prowhooper.com/double-rolling-trippy-spin",
  "https://prowhooper.com/jump-rope",
  "https://prowhooper.com/cinnamon-roll",
  "https://prowhooper.com/burrito-roll",
  "https://prowhooper.com/side-loop",
  "https://prowhooper.com/double-dutch",
  "https://prowhooper.com/flip-stall-rewind",
  "https://prowhooper.com/360-stall-rewind",
  "https://prowhooper.com/matty-stall-rewind",
  "https://prowhooper.com/half-matty-stall-rewind",
  "https://prowhooper.com/540-half-matty-stall-rewind",
  "https://prowhooper.com/building-dive",
  "https://prowhooper.com/wall-ride",
  "https://prowhooper.com/wall-tap",
  "https://prowhooper.com/roll-tap",
  "https://prowhooper.com/loop-tap",
  "https://prowhooper.com/ceiling-tap",
  "https://prowhooper.com/reverse-wall-ride",
  "https://prowhooper.com/downtown-tap",
  "https://prowhooper.com/maverick-tap-rewind",
  "https://prowhooper.com/power-switch-tap",
  "https://prowhooper.com/knife-edge",
  "https://prowhooper.com/reverse-knife-edge",
  "https://prowhooper.com/ninja-star",
  "https://prowhooper.com/face-punch",
  "https://prowhooper.com/slide-disarm",
  "https://prowhooper.com/perch",
  "https://prowhooper.com/eject-roll",
  "https://prowhooper.com/stellar-eject-roll",
  "https://prowhooper.com/blind-flip",
  "https://prowhooper.com/true-barani",
  "https://prowhooper.com/stall-rewind",
  "https://prowhooper.com/beginner-switch",
  "https://prowhooper.com/mavvelmann",
  "https://prowhooper.com/anti-matty",
  "https://prowhooper.com/power-matty",
  "https://prowhooper.com/immelloop",
  "https://prowhooper.com/matty-roll",
  "https://prowhooper.com/immelmatt",
  "https://prowhooper.com/rollani",
  "https://prowhooper.com/flipani"
];

const trickList = document.getElementById('trickList');
const trickButton = document.getElementById('trickButton');

trickButton.addEventListener('click', () => {
  trickList.innerHTML = ''; // Clear previous tricks

  const randomTricks = [];
  for (let i = 0; i < 5; i++) {
    const randomIndex = Math.floor(Math.random() * trickLinks.length);
    randomTricks.push(trickLinks[randomIndex]);
  }

  randomTricks.forEach(trick => {
    const listItem = document.createElement('li');
    const link = document.createElement('a');
    link.href = trick;
    link.textContent = trick.replace("https://prowhooper.com/", ""); // Show only trick name
    link.target = "_blank"; // Open in new tab
    listItem.appendChild(link);
    trickList.appendChild(listItem);
  });
});
</script>

</body>
</html>

<p>
This code creates a webpage with a button that, when clicked, displays five random FPV tricks.<br><br>
Each click will give you a new set of five tricks.<br>
Each trick is a link that opens in a new tab. The `prowhooper.com` part is removed from the displayed link for better readability.<br>
<br>
To add your own links and use this code offline:<br>
**Save:** Save the code as an HTML file (e.g., `RandomFPVTrickGenerator`).<br>
**Open:** Open the HTML file in a web browser.<br>
<br>
To edit links right click the saved .html document and 'open with' a text editor, add your links in the links section following the same format, and re-save as a .html document.<br>
</p>

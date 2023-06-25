
HTML structure:

```
<!DOCTYPE html>
<html>
    <head>
        <title>Tekken 2 Game</title>
        <style>
            /* Add CSS styling for the game elements */
        </style>
    </head>
    <body>
        <h1>Tekken 2</h1>
        <canvas id="gameCanvas"></canvas>
        <script src="game.js"></script>
    </body>
</html>
```

JavaScript code:

```
// Set up the canvas for the game
var canvas = document.getElementById("gameCanvas");
var ctx = canvas.getContext("2d");

// Define game variables
var player = {
    x: 50,
    y: 50,
    width: 50,
    height: 50,
    speed: 5
};
var enemy = {
    x: 250,
    y: 50,
    width: 50,
    height: 50,
    speed: 5
};

// Set up game loop
function gameLoop() {
    // Clear canvas
    ctx.clearRect(0, 0, canvas.width, canvas.height);

    // Move player
    if (38 in keysDown) { // up arrow
        player.y -= player.speed;
    }
    if (40 in keysDown) { // down arrow
        player.y += player.speed;
    }
    if (37 in keysDown) { // left arrow
        player.x -= player.speed;
    }
    if (39 in keysDown) { // right arrow
        player.x += player.speed;
    }

    // Move enemy
    if (player.x < enemy.x) {
        enemy.x -= enemy.speed;
    }
    else {
        enemy.x += enemy.speed;
    }

    // Draw player and enemy
    ctx.fillStyle = "blue";
    ctx.fillRect(player.x, player.y, player.width, player.height);

    ctx.fillStyle = "red";
    ctx.fillRect(enemy.x, enemy.y, enemy.width, enemy.height);
}

// Handle keyboard input
var keysDown = {};
addEventListener("keydown", function (e) {
    keysDown[e.keyCode] = true;
}, false);
addEventListener("keyup", function (e) {
    delete keysDown[e.keyCode];
}, false);

// Start game loop
setInterval(gameLoop, 30);
```

```
<!DOCTYPE html>
<html>
    <head>
        <title>Tekken 2 Game</title>
        <style>
            /* Add CSS styling for the game elements */
        </style>
    </head>
    <body>
        <h1>Tekken 2</h1>
        <canvas id="gameCanvas"></canvas>
        <script src="game.js"></script>
    </body>
</html>
```

JavaScript code:

```
// Set up the canvas for the game
var canvas = document.getElementById("gameCanvas");
var ctx = canvas.getContext("2d");

// Define game variables
var player = {
    x: 50,
    y: 50,
    width: 50,
    height: 50,
    speed: 5
};
var enemy = {
    x: 250,
    y: 50,
    width: 50,
    height: 50,
    speed: 5
};

// Set up game loop
function gameLoop() {
    // Clear canvas
    ctx.clearRect(0, 0, canvas.width, canvas.height);

    // Move player
    if (38 in keysDown) { // up arrow
        player.y -= player.speed;
    }
    if (40 in keysDown) { // down arrow
        player.y += player.speed;
    }
    if (37 in keysDown) { // left arrow
        player.x -= player.speed;
    }
    if (39 in keysDown) { // right arrow
        player.x += player.speed;
    }

    // Move enemy
    if (player.x < enemy.x) {
        enemy.x -= enemy.speed;
    }
    else {
        enemy.x += enemy.speed;
    }

    // Draw player and enemy
    ctx.fillStyle = "blue";
    ctx.fillRect(player.x, player.y, player.width, player.height);

    ctx.fillStyle = "red";
    ctx.fillRect(enemy.x, enemy.y, enemy.width, enemy.height);
}

// Handle keyboard input
var keysDown = {};
addEventListener("keydown", function (e) {
    keysDown[e.keyCode] = true;
}, false);
addEventListener("keyup", function (e) {
    delete keysDown[e.keyCode];
}, false);

// Start game loop
setInterval(gameLoop, 30);
```

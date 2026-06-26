EasyP5jsPlayer is a simple p5js library aimed at getting users started quickly with making a player object for their game

installation:
In your projects index.html file, paste this in
<script src="https://cdn.jsdelivr.net/gh/AvidAndAmateur/EasyP5jsPlayer@main/player.js"></script>
this ensures the library is loaded and findable

usage:
once the player object is made for example lets say you have made a variable named player, you would create the object using
player = makePlayer();

to set the player health you would then do, where x is the desired amount
player.setHealth(x)

To set the player image you would do , where img is your image variable containing your loadimage
player.setImage(img);

To show the player on the screen you would do, where x is the desired width of the image and y is the desired height
player.show(x,y);

To make the player move ensure the that player.movement is in draw function like so:
function draw(){
  //your code
  player.movement();
}

To use the border return (seen in some 2d indie games where the player returns to the screen in the opposite direction they went in)
use the following:
function draw(){
  //your code
  player.checkmap();
}
example style.js:
let imgy;
function preload(){
  imgy = loadImage("imagelink/file");
}
function setup() {
    createCanvas(400, 400);
    p = makePlayer();
}

function draw() {
    background(220);
    p.setImage(imgy)
    p.movement();
    p.show(50,50);
}

# Quiz8
**Part 1: Imaging Technique Inspiration**

*Imaging Technique Choice*

I drew inspiration from the visual elements of My Neighbor Totoro, directed by Hayao Miyazaki. The film often showcases soft, natural landscapes and lively cartoon characters, particularly the scenes where the wind gently moves through the grass, creating a soothing and dreamlike atmosphere. The gentle, rhythmic motion of nature adds a sense of peace and wonder to the animation.

*Why Choose It*

The natural vitality and innocence in My Neighbor Totoro is captivating, and I want to replicate similar dynamic effects to convey that sense of warmth and softness. By simulating the effect of wind blowing through grass, I can create an adorable, lively animated scene that mirrors the serene beauty of nature depicted in Miyazaki’s works.

![An animated Totoro](week8/Totoro.GIF)

**Part 2: Coding Technique Exploration**

*Coding Technique Choice*

To recreate the dynamic grass-blowing effect from My Neighbor Totoro, I’ve chosen Perlin noise as the driving force behind the movement. Perlin noise generates smooth, continuous waves that mimic the fluid motion of nature, such as grass swaying in the wind. This method can bring life and movement to the scene while maintaining the gentle and tranquil feel characteristic of Miyazaki’s films.

*Why Choose It*

Perlin noise is ideal for creating smooth, organic motion, perfect for simulating the subtle, flowing movements of natural elements like grass. This technique can bring out the natural beauty and liveliness of the scene, reflecting the peaceful yet dynamic nature found in Miyazaki’s works.

*Reference Code*

let xoff = 0;
let yoff = 0;

function setup() {
  createCanvas(400, 400);
  background(135, 206, 250); 
}

function draw() {
  background(135, 206, 250);
  stroke(34, 139, 34);
  noFill();

  beginShape();
  for (let x = 0; x < width; x += 10) {
    let y = map(noise(xoff, yoff), 0, 1, 200, 300);
    vertex(x, y);
    xoff += 0.05;
  }
  endShape();

  yoff += 0.01; // Simulating gentle wind motion
}



int circles;
float dist, radius, step, angle;
PVector[] centers;
int[] colorIndex;

void setup() {
  size(400, 400);
  colorMode(HSB);
  noFill();
  strokeWeight(3);
 
  circles = 8;
  angle = 0;
  step = TWO_PI / circles;
  radius = 16;
  dist = 64;
  centers = new PVector[circles];
  colorIndex = new int[circles];

  for (int i = 0; i < 8; i++, angle += step) {
    centers[i] = new PVector(dist * cos(angle) + width / 2, dist * sin(angle) + height / 2);
  }

  for (int i = 0; i < colorIndex.length; i++)
    colorIndex[i] = i;
}

void draw() {
  background(0);

  for (int i = 0; i < centers.length; i++) {
    stroke(map(colorIndex[i], 0, colorIndex.length, 0, 255), 255, 255);
    ellipse(centers[i].x, centers[i].y, radius * 2, radius * 2);
    if (frameCount % 4 == 0) {
      colorIndex[i] = (colorIndex[i] + 1) % colorIndex.length;
    }
  }
}

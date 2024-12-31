# Spot-leather
Happy new year

![buh](https://github.com/nicolasbaez/Spot-leather/blob/main/xp045.gif)
```javascript
setup = (_) => createCanvas((w = 500), w);
r = (n) => random(n);
g = (x, y, a) => {
  stroke(x, y, w);
  line(x, y, x, y - r(a));
  s = r();
  ellipse(x, y, a * s, (a * s) / 3);
  ellipse(x, y, a, a / 3);
};
draw = (_) => {
  colorMode(HSB, w);
  background(0, 9);
  g(r(w), r(w), r(99));
  fill(r(w), 99);
  if (sin(w) > 0.9) rect(0, 0, w, w);
  if (w == 500) saveGif("xp045.gif", 1884, { delay: 0, units: "frames" });
  w += 0.01;
};

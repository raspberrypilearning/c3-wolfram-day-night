## Building a Map

--- task ---
If you have never used the Wolfram Language before, follow [this guide](https://projects.raspberrypi.org/en/projects/getting-started-with-mathematica) to get started and learn to use the tool. You'll need to look at **Starting Mathematica** and **Programming in Mathematica**.
--- /task ---

In this step, you will build a map, find the Night Hemisphere, and highlight a specific country.

--- task ---

Create a map using `GeoGraphics[]` and specifying the region you want to show.

```
GeoGraphics[GeoRange -> "World"]
```
![Simple Map](images/map1.png)

--- /task ---

The NightHemisphere function shades the part of the Earth which is currently in nighttime.

--- task ---

Add the Night Hemisphere to your map. Replace your previous code with your new code.

```GeoGraphics[NightHemisphere[], GeoRange -> "World"]```

![Night Hemisphere](images/DayNight.png)

--- /task ---
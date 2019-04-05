## Build a map

--- task ---
If you have never used the Wolfram Language before, follow [this guide](https://projects.raspberrypi.org/en/projects/getting-started-with-mathematica) to get started and learn to use the tool. You'll need to look at **Starting Mathematica** and **Programming in Mathematica**.
--- /task ---

In this step, you will build a map and find the night hemisphere.

--- task ---

Create a map using `GeoGraphics[]`, specifying the region you want to show.

```
GeoGraphics[GeoRange -> "World"]
```
![Simple Map](images/map1.png)

--- /task ---

The `NightHemisphere` function shades the part of the Earth where it currently is nighttime.

--- task ---

Add the night hemisphere to your map by replacing your code with the following line:

```
GeoGraphics[NightHemisphere[], GeoRange -> "World"]
```

![Night Hemisphere](images/DayNight.png)

--- /task ---
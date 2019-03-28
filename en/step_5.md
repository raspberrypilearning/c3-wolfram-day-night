## Make your map interactive

What if you don't want to see information for the country that is highlighted right now? It would be a lot of effort to change the code every time you want to see a different country. Instead, you can set up a drop-down menu that allows your user to choose a country.

To make a drop-down menu of countries, you need a list of every country in the world. Luckily, Wolfram has one built in!

```
CountryData[]
```
![Country Data](images/CountryData.png)

With `Manipulate`, you can make an interactive drop-down menu. `Manipulate` lets you set `x` as a placeholder. The user can then replace `x` with a value. In order to create a `Manipulate` statement, you need a function with a placeholder variable and a list of possibilities for `x`.

--- task ---
Move the code that creates the map highlighting the USA **inside** a `Manipulate` statement, with the options for the `Polygon` coming from `CountryData`.

 ```
 Manipulate[
 GeoGraphics[
  {NightHemisphere[],
   {EdgeForm[Yellow],
    FaceForm[Gray],
    Polygon[x]}
   },
  GeoRange -> "World"],
 {x, CountryData[]}
 ]
 ```
--- /task ---

If you find that it takes too long to load the country data, try using `CountryData["G20"]` instead. This should be faster because it loads a shorter list of countries.

--- task ---

Make the map a little more eye-catching by changing the edge of the highlighted country to black and filling it with red.

--- hints ---
--- hint ---
The `EdgeForm` and `FaceForm` functions set the colours.
--- /hint ---
--- hint ---
You can see these functions in the code you already have:

```
EdgeForm[Yellow],
FaceForm[Gray],
```
--- /hint ---
--- /hints ---
--- /task ---

Now you can select any country, and the map will change to highlight your selection!
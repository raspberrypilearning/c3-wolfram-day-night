## Making your Map Interactive

So far, you've created a world map with the day and night hemispheres, where you can see a specific country. But what if you don't want to see information for the United States? It would take too much effort to change the code every time you wanted to see a different country. You could set up a little tool which allows your user to chose a country from a drop down menu.

In order to make a drop down menu of countries, we're going to need a list of every country in the world. Luckily, Wolfram has one built in!

```
CountryData[]
```
![Country Data](images/CountryData.png)

We can use `Manipulate` to make an interactive drop down list. `Manipulate` lets us use x as a placeholder, and then to replace x with a value that the user chooses. In order to create a `Manipulate`, we need to have a function with a placeholder variable, and a list of possibilities for what x could be.

--- task ---

 Incorporate the code you used to create the map highlighting the USA into a `Manipulate`, with the options for the polygon shape coming from `CountryData`.
 
 ```
 Manipulate[
 GeoGraphics[
  {NightHemisphere[],
   {EdgeForm[Black],
    FaceForm[Red],
    Polygon[x]}
   },
  GeoRange -> "World"],
 {x, CountryData[]}
 ]
 
 ```
--- /task ---

If you are using Wolfram in a browser, you may find that this takes a minute or so to run.

Now we can select any country, and the map will change to highlight our selection!
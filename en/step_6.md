## Add information to your map

In this step, you're going to add a `Dynamic` sentence to your map. This sentence will contain information about the country the user selects.

`Dynamic` allows you to use the value that placeholder in `Manipulate` represents.

--- task ---
First, create a `Dynamic` sentence that displays the name of the country selected from the drop-down menu.

```
 Manipulate[
 GeoGraphics[
  {NightHemisphere[],
   {EdgeForm[Black],
    FaceForm[Red],
    Polygon[x]}
   },
  GeoRange -> "World"],
 {x, CountryData[]},
 Dynamic[CountryData[x, "Name"]]
 ]
 ```

![Manipulate with Dynamic Country Name](images/ManipulateName.png)

Select a different country from the drop-down menu and check that the `Dynamic` name changes.

--- /task ---

Now you have a `Dynamic` object in your `Manipulate` function, you can make it more useful. As an example, you can add a sentence stating whether the highlighted country is in daytime or nighttime. Use the function `DaylightQ` to do this.

+ `DaylightQ` asks the system if it's daytime or not, and outputs either `True` or `False`.

+ `DaylightQ` only works with a city name, rather than a country name.

You can find all the cities in a country by using `CityData`.

```
CityData[{All, CountryData[Entity["Country", "Togo"], "Name"]}]

```
![City Data](images/CityData.png)

`CityData` lists cities in order of size. Therefore, the `First` item in a `CityData` list is always the largest city in a country.

```
First[CityData[{All, CountryData[Entity["Country", "Togo"], "Name"]}]]

```

--- task ---
Add code to the `Dynamic` function so that the function also says `True` if the largest city in the highlighted country is in daytime, or `False` if the city is in nighttime.

You know how to use a list, with `{}`, to ask `GeoGraphics` to do multiple things at the same time. And you can do the same with `Dynamic`.

Replace your code with this new code:

```
Manipulate[
 GeoGraphics[
 {NightHemisphere[],
 {EdgeForm[Black],
 FaceForm[Red],
 Polygon[x]}},
 GeoRange -> "World"],
 {x, CountryData[]}, 
 Dynamic[
 {CountryData[x, "Name"],
 DaylightQ[First[CityData[{All, CountryData[x, "Name"]}], 1]]}]
 ]
 ```
 
![Manipulate with Day Night Information](images/ManipulateInfo.png)
 
--- /task ---
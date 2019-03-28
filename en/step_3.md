## Highlight a country

Now, highlight a country. The United States of America are the example here, but you can choose any country. Only make sure that the country you choose is large enough to be seen clearly on the map.

--- task ---
Press <kbd>Control</kbd>  and <kbd>=</kbd> at the same time to access a Free-Form Input box directly within your code. Into this box, you can type the name of a country or city.

![FreeForm Linguistic Input](images/FreeForm.png)

Type 'United States' into the Input box to highlight the United States on the map.

```
GeoGraphics[Polygon[United States], GeoRange -> "World"]
```

![Country Polygon](images/Polygon.png)
--- /task ---

At the moment, the highlight is just grey. A more visible colour would be better.

--- task ---
+ Change the colour of the highlighted country to red using `FaceForm`
+ Add black edges using `EdgeForm`

```
GeoGraphics[{EdgeForm[Black], FaceForm[Red], Polygon[United States]}, 
 GeoRange -> "World"]
 ```
![Country Polygon](images/RedPolygon.png)

--- /task ---

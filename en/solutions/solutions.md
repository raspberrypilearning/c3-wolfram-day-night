 ```
 Manipulate[
 GeoGraphics[
 {NightHemisphere[],
 EdgeForm[Black],
 FaceForm[Red],
 Polygon[x]},
 GeoRange -> "World"],
 {x, CountryData[]}, 
 Dynamic[
 If[DaylightQ[First[CityData[{All, CountryData[x, "Name"]}], 1]],
 Row[{
 "It's daytime in ",
 CountryData[x, "Name"],
 ". Sunset will be at: ",
 TimeObject[Sunset[First[CityData[{All, CountryData[x, "Name"]}], 1]]]
 }],
 Row[{"It's nighttime in ",
 CountryData[x, "Name"],
 ". Sunrise will be at: ",
 TimeObject[Sunrise[First[CityData[{All, CountryData[x, "Name"]}], 1]]]
 }]
 ]]
 ]

```

Challenge

This challenge cannot be completed in the browser version of Wolfram. Please use the desktop application.

```
Manipulate[
 GeoGraphics[
  {
   NightHemisphere[],
   EdgeForm[Black],
   FaceForm[Red],
   Tooltip[
    Polygon[x],
    If[DaylightQ[First[CityData[{All, CountryData[x, "Name"]}], 1]],
     Row[{"It's Daytime in ", CountryData[x, "Name"], 
       "! Sunset is at: ", 
       TimeObject[
        Sunset[First[CityData[{All, CountryData[x, "Name"]}], 1]]]}],
      Row[{"It's Nighttime in ", CountryData[x, "Name"], 
       "! Sunrise is at: ", 
       TimeObject[
        Sunrise[First[CityData[{All, CountryData[x, "Name"]}], 
          1]]]}]]
    ]
   },
  GeoRange -> "World"],
 {x, CountryData[]}
 ]
 ```

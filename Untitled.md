---
title: "Map"
author: "Amelia Renner"
date: "3/5/2022"
output: 
  html_document:
    keep_md: TRUE
    toc: TRUE
    toc_float: TRUE
    df_print: paged
    code_download: true
    code_folding: hide 
---







```r
favorites <- tibble(
  place = c("Eggsperience", "Grandpa's House", "Jesus's House", 
            "Secret Garden", "Conservatory", "Gethsemane",
            "Aquarium", "Thrift Store", "Smoothie Place", 
            "Jewel", "La Micho", "Plant Store"),
  long = c(-87.6603503, -87.6351444, -87.64986835971123, -87.63386807651638, -87.63533023001932, -87.66900348395929, -87.6139951147024, -87.66810894072653, -87.62440176866743, -87.64524342209727, -87.6619222914252, -87.66379419937428
           ),
  lat = c(41.8695086, 41.9083356, 41.840493733150666, 41.92500851762896, 41.92497795915031, 41.98753273753473, 41.868243394672476, 41.925358403457864, 41.87752079725744, 41.8894549679426, 41.857437372127094, 41.83546008876618
         )
  )
```



```r
leaflet(data = favorites) %>% 
  addTiles() %>% 
  addMarkers(lng = ~long, 
             lat = ~lat, 
             label = ~place)
```

```{=html}
<div id="htmlwidget-9978effb792d6dd9fd68" style="width:672px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-9978effb792d6dd9fd68">{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"calls":[{"method":"addTiles","args":["//{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":1,"detectRetina":false,"attribution":"&copy; <a href=\"http://openstreetmap.org\">OpenStreetMap<\/a> contributors, <a href=\"http://creativecommons.org/licenses/by-sa/2.0/\">CC-BY-SA<\/a>"}]},{"method":"addMarkers","args":[[41.8695086,41.9083356,41.8404937331507,41.925008517629,41.9249779591503,41.9875327375347,41.8682433946725,41.9253584034579,41.8775207972574,41.8894549679426,41.8574373721271,41.8354600887662],[-87.6603503,-87.6351444,-87.6498683597112,-87.6338680765164,-87.6353302300193,-87.6690034839593,-87.6139951147024,-87.6681089407265,-87.6244017686674,-87.6452434220973,-87.6619222914252,-87.6637941993743],null,null,null,{"interactive":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},null,null,null,null,["Eggsperience","Grandpa's House","Jesus's House","Secret Garden","Conservatory","Gethsemane","Aquarium","Thrift Store","Smoothie Place","Jewel","La Micho","Plant Store"],{"interactive":false,"permanent":false,"direction":"auto","opacity":1,"offset":[0,0],"textsize":"10px","textOnly":false,"className":"","sticky":true},null]}],"limits":{"lat":[41.8354600887662,41.9875327375347],"lng":[-87.6690034839593,-87.6139951147024]}},"evals":[],"jsHooks":[]}</script>
```

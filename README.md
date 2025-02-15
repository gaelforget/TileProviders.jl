# TileProviders

[![Stable](https://img.shields.io/badge/docs-stable-blue.svg)](https://rafaqz.github.io/TileProviders.jl/stable/)
[![Dev](https://img.shields.io/badge/docs-dev-blue.svg)](https://rafaqz.github.io/TileProviders.jl/dev/)
[![Build Status](https://github.com/rafaqz/TileProviders.jl/actions/workflows/CI.yml/badge.svg?branch=main)](https://github.com/rafaqz/TileProviders.jl/actions/workflows/CI.yml?query=branch%3Amain)
[![Coverage](https://codecov.io/gh/rafaqz/TileProviders.jl/branch/main/graph/badge.svg)](https://codecov.io/gh/rafaqz/TileProviders.jl)

Provider map tiles in a `Provider` object.

Complete urls to tiles can be retrieved with `geturl(provider::Provider, x::Int, x::Integer, z::Integer)`.


A custom provider can be provided with:

```julia
using TileProviders
Provider("http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png")
```

Many providers are available in the package, loaded with:

```julia
AzureMaps()
BasemapAT()
CartoDB()
CyclOSM()
Esri()
FreeMapSK()
GeoportailFrance()
Google()
HERE()
HEREv3()
HikeBike()
Jawg()
JusticeMap()
MapBox()
MapTiler()
MapTilesAPI()
MtbMap()
NASAGIBS()
NLS()
OPNVKarte()
OneMapSG()
OpenAIP()
OpenFireMap()
OpenRailwayMap()
OpenSeaMap()
OpenSnowMap()
OpenStreetMap()
OpenTopoMap()
OpenWeatherMap()
SafeCast()
Stadia()
Stamen()
SwissFederalGeoportal()
Thunderforest()
TileProviders()
TomTom()
USGS()
WaymarkedTrails()
geturl()
nlmaps()
```

Some providers will need an `apikey` or `accestoken` keyword if registration
is required to use the dataset. See the docs for the function.

Providers are retrieved from leaflet via geopandas repository:
https://raw.githubusercontent.com/geopandas/xyzservices/main/provider_sources/leaflet-providers-parsed.json

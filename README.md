# Geocode [![Build Status](https://secure.travis-ci.org/NewMotion/scala-geocode.png)](http://travis-ci.org/NewMotion/scala-geocode)

Google [geocode api](https://developers.google.com/maps/documentation/geocoding) client written in Scala


## Supports

* Getting geocode responses for a gps coordinates

## Example

```scala
      val geocode = new Geocode()
      geocode ? Location(51.498685, -0.12967) foreach {
            case Right(results) => results.foreach(r => println(r.formatted_address))
            case Left(error) => println(error)
      }

//      4B Deans Yd, Westminster, London, Greater London SW1P 3NP, UK
//      Westminster Abbey (Stop W), Westminster, City of Westminster, London SW1P, UK
//      Westminster, Westminster Abbey (S-bound), Westminster, City of Westminster, London SW1P, UK
//      Westminster, Westminster Abbey (Stop X), Westminster, City of Westminster, London SW1P, UK
//      Westminster Abbey (R), Westminster, City of Westminster, London SW1H, UK
//      Westminster, City of Westminster, London SW1P 3NY, UK
//      London, Greater London SW1P, UK
//      Westminster, London, UK
//      City of Westminster, Greater London, UK
//      London, UK
//      London, UK
//      Greater London, UK
//      England, UK
//      United Kingdom
```


## Setup

1. Add this resolver to your build file:
```
resolvers += "TNM" at "http://nexus.thenewmotion.com/content/groups/public"
```

2. Add dependency to your build file:
```"com.thenewmotion" %% "scala-geocode" % "2.3"```

## Contributors

Georgii Leontiev  
Maxim Fedorov  
Reinier Lamers  
Yaroslav Klymko
https://github.com/speedcom

---
layout: post
title: "iuno German"
---
![alternativtext](\iuno-blog\images\zero.jpg)

## Einleitung
`***///Hier Einleitung///***`

## Verwendete Programme
* Intellij
* Git
* Thonny
* Postman
* Proxmox 8 (Server OS)
* PostgerSQL
* pgAdmin
* draw.io (Planung)
* ioBroker (für Datenpunkte von Smart Home Geräten)
* Zigbee USB Stick
* Telegram
* Grafana

## Verwendete Hardware
* Raspberry Pi 4
* Raspberry Pi Pico
* Raspberry Pi Zero
* [Server](https://22ronny.github.io/server-blog/2024/01/18/Eigenbau-Server.html)
* Temperatursensor
* Türkontakt
* Taster


## Datenbank
#### PostgreSQL
Die Datenbank wurden in einem LXC erstellt.  
* mit Proxmox (Debian Bookworm - Eigener Server)   

## Raspberry´s  



## Highlights
`***///Highlights///***`

* **Dynamische Abfragen:**  
 Ermöglicht das Erstellen von Abfragen, die auf variablen Filterkriterien basieren. Dies ist besonders nützlich, wenn Anwendungen flexibel auf Benutzeranfragen reagieren müssen.

* **Wiederverwendbarkeit:**  
 Die Methode kann in verschiedenen Teilen der Anwendung wiederverwendet werden, um unterschiedliche Abfragen mit ähnlichen Filterlogiken zu erstellen, ohne dass jedes Mal eine neue Methode geschrieben werden muss.

* **Anpassbarkeit:**  
 Erlaubt Benutzern oder anderen Teilen der Anwendung, die Datenbankabfrage dynamisch anzupassen, indem sie nur die relevanten Filterparameter ändern.

  
Controller:
```java
    @RequestMapping("/getCatch")
    List<CatchDto> getCatch(
            @RequestParam(required = false) Long fishTypeId,
            @RequestParam(required = false) LocalDateTime startDate,
            @RequestParam(required = false) LocalDateTime endDate,
            @RequestParam(required = false) Long speciesId,
            @RequestParam(required = false) Long baitId,
            @RequestParam(required = false) Long placeId) {
        return service.getCatch(fishTypeId, startDate, endDate, speciesId, baitId, placeId);
    }
```


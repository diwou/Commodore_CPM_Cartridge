# Commodore CP/M Cartridge für den Commodore C64

![](https://codeberg.org/diwou/Commodore_CPM_Cartridge/raw/branch/main/Images/Commodore_CPM_Cartridge.jpg)

Dies ist ein Nachbau der Commodore CP/M-Cartridge, mit der es möglich war, CP/M in Version 2.2 zu verwenden.

## Einführung

Im Rahmen meines anderen Z80-Cartridge-Projekts hier auf GitHub hatte ich zunächst die originale Commodore CP/M-Cartridge zu Analysezwecken nachgebaut.

Ich habe mich dabei so nah wie möglich an das Originallayout gehalten und nur ein paar Footprints an die aktuelle Teileverfügbarkeit angepasst. Die Platine ist in Abmessungen und Bohrungen identisch zur Originalplatine und passt daher auch ins Gehäuse der Commodore-Version.

Aufgrund der 1:1-Reproduktion hat diese Cartridge natürlich auch alle entsprechenden „Probleme“ hinsichtlich der Kompatibilität.

Ich konnte die Karte sowohl in einer 407er- als auch in einer 469er-Platine problemlos betreiben. Der verwendete VIC spielte offenbar keine Rolle.

Die verwendeten Komponenten auf der CP/M-Platine hingegen schon.

Normalerweise sind „LS“-Typen stabiler als andere Varianten. In einem meiner Tests konnte ich mit „S“-Typen keine stabile Funktion erreichen.

## Komponenten

Die gesamte Schaltung besteht nur aus ein paar TTL-Bausteinen und einem 4 MHz-Quarz. Die Software liegt auf einer 2732-EPROM.

Die Belegung der EPROM ist gleich zur Original-Cartridge. Ein passendes Abbild liegt dem Repository bei.

Einige der TTLs sind mit dem C64 verbunden und teilweise „zeitkritisch“ zu behandeln. Andere steuern lediglich das Reset, Clock-Handling oder die Chip-Select-Signale.

Die Unterschiede zu meiner neueren Z80-Cartridge bestehen vor allem in der Art der Ansteuerung, in der Taktverarbeitung und im Timing.

Das Board hat im Test sehr zuverlässig funktioniert – unter der Voraussetzung, dass exakt passende Bauteile verwendet wurden. Bereits kleine Abweichungen, z. B. ein anderer Hersteller, können zu Instabilitäten führen.

## Hinweise

Da es sich um eine 1:1-Rekonstruktion handelt, dient diese Platine vor allem zu historischen bzw. Vergleichszwecken.

Wer eine stabile und moderne Lösung für CP/M auf dem C64 sucht, sollte sich die [Z80-Karte für den Commodore C64](https://codeberg.org/diwou/Z80-Card_for_Commodore_C64) ansehen.

Diese bietet deutlich höhere Stabilität, volle 8 MHz Z80-Taktung und ist in CPLD-Technik realisiert, wodurch die Probleme der Originalversion umgangen werden.

## Lizenz

Der Inhalt dieses Repositories steht unter der folgenden Lizenz:

**Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)**  
Der vollständige Lizenztext befindet sich in der Datei [LICENSE.CC-NC-BY-SA-4.0](https://codeberg.org/diwou/Commodore_CPM_Cartridge/raw/branch/main/LICENSE.CC-NC-BY-SA)  
Und ist auch online verfügbar unter: https://creativecommons.org/licenses/by-nc-sa/4.0/

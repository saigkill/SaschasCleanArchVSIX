# Clean Architecture Konsole

Dieses Projekt ist eine Visual Studio Extension (Projektvorlage) bereitgestellt. Es ist ein einfaches Konsolenanwendung-Projekt, das auf der Clean Architecture basiert.

|What|Status|
|---|---|
|Language|C#|
|Framework|.NET 8|
|Latest Release| [![Latest Release](https://gitlab.infas.de/it-entwicklung/cleanarchitecturekonsolevsix/-/badges/release.svg)](https://gitlab.infas.de/it-entwicklung/cleanarchitecturekonsolevsix/-/releases)|

## Authors

- [@Sascha](https://gitlab.infas.de/a13007)

## Ver�ffentlichung

Die Anwendung wird als Visual Studio Extension bereitgestellt.
Die Projektvorlage kann hier installiert werden: \\srvfile005vm\Basics\IT_Intern\Sascha\VSExtensions\CleanArchitectureConsole

## Documentation

In Program.cs wird ein Hostservice eingerichtet (`ConsoleService`). Dieser Schritt wurde erwogen, um sowohl Dependency Injection, als auch die Konfiguration �ber ein JSON File zu erm�glichen. Ebenso erfolgt eine saubere
Inititlisierung und Beendingung der Anwendung via AppLifetime.

## Konfiguration

Die Konfiguration erfolgt �ber die Datei `appsettings.json`. Hier k�nnen die Datenbankverbindung und der Pfad zur CSV-Datei angepasst werden.

Es wird eine `nlog.config` mit ausgeliefert, die die Konfiguration des Loggings �bernimmt.

## Error Handling

Wir nutzen das NLog-Framework zum loggen der Fehler. Die Konfiguration hierf�r ist in der Datei `nlog.config` hinterlegt. 

Errors und Exceptions werden in Infas-eigener Sentry-Instanz geloggt und die betroffenen Entwickler informiert.


## 3rd Party Libraries

Wir nutzen die folgenden 3rd Party Libraries:

* Fluent Validator
* NLog

## Changelog

Wir nutzen die [Tags](https://gitlab.infas.de/it-entwicklung/cleanarchitecturekonsolevsix/-/tags) um �nderungen an der Anwendung zu dokumentieren.

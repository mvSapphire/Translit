# NickBuhro.Translit

C# library for cyrillic-latin transliteration.

[![License](https://img.shields.io/badge/license-MIT-red.svg)](https://raw.githubusercontent.com/nick-buhro/Translit/master/LICENSE)
[![NuGet Badge](https://buildstats.info/nuget/NickBuhro.Translit)](https://www.nuget.org/packages/NickBuhro.Translit/)
[![Build status](https://ci.appveyor.com/api/projects/status/5xxmbn82hu9762n7?svg=true)](https://ci.appveyor.com/project/nick-buhro/translit)
[![Coverage Status](https://coveralls.io/repos/github/nick-buhro/Translit/badge.svg?branch=master)](https://coveralls.io/github/nick-buhro/Translit?branch=master)

## Features

It implements transliteration by 
[ISO 9](https://en.wikipedia.org/wiki/ISO_9) 
([ГОСТ 7.79—2000](https://ru.wikipedia.org/wiki/ISO_9#.D0.93.D0.9E.D0.A1.D0.A2_7.79.E2.80.942000)) 
on System B (only for slavik languages).

Both direction transliteration is supported:
* cyrillic to latin
* latin to cyrillic

It could be specified concrete language from list:
* Russian
* Belorussian
* Ukrainian
* Bulgarian
* Makedonian

## Usage

``` C#

// Cyrillic to latin example

var latin = Transliteration.CyrillicToLatin("Предками данная мудрость народная!", Language.Russian);
Console.WriteLine(latin);	// Output: Predkami dannaya mudrost` narodnaya!

// Latin to cyrillic example

var cyrillic = Transliteration.LatinToCyrillic("Predkami dannaya mudrost` narodnaya!", Language.Russian);
Console.WriteLine(cyrillic);	// Output: Предками данная мудрость народная!

```

## Compatibility

The library uses no references except for `System` - it has no external dependencies.
It is cross compiled to:

* .NET Framework 2.0 and above
* .NET Standard 1.3

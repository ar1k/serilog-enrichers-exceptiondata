# Serilog.Enrichers.ExceptionData

## ExceptionDataEnricher

Enriches Serilog events with collection of key/value pairs from exception's `Data` property.
 
To use the enricher, first install the NuGet package:

```powershell
Install-Package Serilog.Enrichers.ExceptionData
```

Then, apply the enricher to you `LoggerConfiguration`:

```csharp
Log.Logger = new LoggerConfiguration()
    .Enrich.WithExceptionData()
    // ...other configuration...
    .CreateLogger();
```

The `WithExceptionData()` enricher will add a properties from exception's `Data` property to produced events.

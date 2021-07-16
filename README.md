# Weather Forecast Apis - Http & Https
This sample project can simulate the sceneario described [here](https://github.com/Kong/kong/issues/7566#issuecomment-881134190).

# Needs
- [.NET SDK 5.xxx](https://dotnet.microsoft.com/download/dotnet/5.0) - choose your OS.

To run it, you can use your favorite IDE that compiles .NET, like [Visual Studio Code](https://code.visualstudio.com/) with [OmniSharp](https://code.visualstudio.com/docs/languages/csharp) plugin.


## Run HTTP Api version

 `YOUR_CLONE_FOLDER\WeatherForecast.Api.Http> dotnet run`

```
Building...
info: Microsoft.Hosting.Lifetime[0]
      Now listening on: http://localhost:7000
info: Microsoft.Hosting.Lifetime[0]
      Application started. Press Ctrl+C to shut down.
info: Microsoft.Hosting.Lifetime[0]
      Hosting environment: Development
info: Microsoft.Hosting.Lifetime[0]
      Content root path: I:\_projects\net\weatherforecast-apis\WeatherForecast.Api.Http
```

> GET: `http://localhost:7000/health`

## Run HTTPs Api version

 `YOUR_CLONE_FOLDER\WeatherForecast.Api.Https> dotnet run`

```
Building...
info: Microsoft.Hosting.Lifetime[0]
      Now listening on: https://localhost:5001
info: Microsoft.Hosting.Lifetime[0]
      Now listening on: http://localhost:5000
info: Microsoft.Hosting.Lifetime[0]
      Application started. Press Ctrl+C to shut down.
info: Microsoft.Hosting.Lifetime[0]
      Hosting environment: Development
info: Microsoft.Hosting.Lifetime[0]
      Content root path: I:\_projects\net\weatherforecast-apis\WeatherForecast.Api.Https
```

> GET: `https://localhost:5001/health`


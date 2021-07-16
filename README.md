# Weather Forecast Apis - Http & Https
This sample project can simulate scenery described [here](https://github.com/Kong/kong/issues/7566#issuecomment-881134190).

# Needs

- [.NET SDK 5.xxx](https://dotnet.microsoft.com/download/dotnet/5.0) - choose your OS.

To run it, you can use your favorite IDE that compiles .NET, like [Visual Studio Code](https://code.visualstudio.com/) with [OmniSharp](https://code.visualstudio.com/docs/languages/csharp) plugin.

# 

## Https on localhost

To run localhost with HTTPs, we need to set/add some "dev" certs to able it. We can able this with this simple commands:

### [All platforms - certificate not trusted](https://docs.microsoft.com/en-us/aspnet/core/security/enforcing-ssl?view=aspnetcore-5.0&tabs=visual-studio#all-platforms---certificate-not-trusted)
```
<ON_ANY_FOLDER_AFTER_INSTALL_NET_SDK\...\> dotnet dev-certs https --clean
<ON_ANY_FOLDER_AFTER_INSTALL_NET_SDK\...\> dotnet dev-certs https --trust
```
If you are having problems with those commands, please see the following link to troubleshoot certificate problems, specifics configs by OS(Linux/Docker, macOS, Windows): [Enforce HTTPS in ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/security/enforcing-ssl?view=aspnetcore-5.0&tabs=visual-studio).

# 

## Run HTTP Api version

```
 YOUR_CLONE_FOLDER\weatherforecast-apis\WeatherForecast.Api.Http> dotnet restore
 YOUR_CLONE_FOLDER\weatherforecast-apis\WeatherForecast.Api.Http> dotnet run
```

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

### TRY
> GET: `http://localhost:7000/health`

# 

## Run HTTPs Api version

```
 YOUR_CLONE_FOLDER\weatherforecast-apis\WeatherForecast.Api.Https> dotnet restore
 YOUR_CLONE_FOLDER\weatherforecast-apis\WeatherForecast.Api.Https> dotnet run
```

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

### TRY
> GET: `https://localhost:5001/health`

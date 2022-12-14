# LineNotifyLogger

### How to use this dependency?
- `dotnet add package LineNotifyLogger`
- setup NotifyLogger in Program.cs file
  ```
  Host.CreateDefaultBuilder(args)
      .ConfigureWebHostDefaults(webBuilder =>
      {
          webBuilder.UseStartup<Startup>();
      })
      .ConfigureLogging((host, logging) =>
      {
          logging.AddNotifyLogger(opt =>
          {
              host.Configuration.GetSection("Logging").GetSection("Notify").GetSection("Options").Bind(opt);
          });
      });
  ```
- add config in appsetting.json file
  ```
    "Logging": {
      "Notify": {
          "Options": {
              "token": "your token"
          }
      }
    }
  ```

# LineNotifyLogger

### How to use this dependency?
- `dotnet add package LineNotifyLogger`
- setup NotifyLogger in Program.cs file
  ```
  using LineNotifyLogger;
  ...
  Host.CreateDefaultBuilder(args)
      .ConfigureWebHostDefaults(webBuilder =>
      {
          webBuilder.UseStartup<Startup>();
      }).LineNotify();
  ```
- add config in appsetting.json file
  ```
    "Logging": {
      "Notify": {
          "Options": {
              "serviceName": "your service name",
              "token": "your token"
          }
      }
    }
  ```

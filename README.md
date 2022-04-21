# ProjectConfigFile / Config.cs use

**Write to the config file**
```csharp
ProjectConfigFile ConfigFile = new ProjectConfigFile("applicationconfig"/*folder path*/, "config"/*ini file name*/, new string[] { "user", "pass" });

ConfigFile["user"] = "testuser"; // These values will be written to the file when they are set by the indexer.
ConfigFile["pass"] = "password123";

ConfigFile[0] = "testuser";
ConfigFile[1] = "password123";
```

**Read values from config file**
```csharp
string username = ConfigFile["user"];
string password = ConfigFile["pass"];
```

**or**
```csharp
string username = ConfigFile[0];
string password = ConfigFile[1];
```

**or**
```csharp
string username = getConfigName(0); // Returns "user"
string password = getConfigValue("pass"); // Returns "password123"
string password = getConfigValue(1); // Also returns "password123"
```

**Get file path and name**
```csharp
string filepath = ConfigFile.FilePath;
string filename = ConfigFile.FileName
```

**Get settings and values as arrays**
```csharp
string[] settingNames = ConfigFile.SettingNames;
string[] settingValues = ConfigFile.SettingValues;
```

# PascalABC.NET Compiler multitarget

Консольный компилятор PascalABC.NET с поддержкой .NET Framework 4.8 и .NET 10.

## 📋 Особенности
- Мультиплатформенная сборка (net48 и net10.0)
- Совместимость с Windows (net48) и кроссплатформенность (net10)
- Поддержка современных возможностей .NET

## 🚀 Сборка

### Требования
- .NET Framework 4.8 Developer Pack
- .NET 10 SDK
- Visual Studio 2026 или новее (опционально)

### Команды
```bash
# Сборка под .NET Framework 4.8
dotnet build -f net48

# Сборка под .NET 10
dotnet build -f net10.0

# Сборка всех платформ
dotnet build

# Visual Studio
Сборка осуществляется под .NET 10.0
```

Для сборки под Net4.8 поменяйте строку 
```
<TargetFramework Condition="'$(BuildingInsideVisualStudio)' == 'true'">net10.0</TargetFramework>
```
на 
```
<TargetFramework Condition="'$(BuildingInsideVisualStudio)' == 'true'">net48</TargetFramework>
```
в `Directory.Build.props`.



### 📁 Структура проекта
```
PascalABC.NET/
├── src/          # Исходный код
├── bin/          # Собранные сборки
└── obj/          # Промежуточные файлы
```

### 🔧 Конфигурация

Проект использует `Directory.Build.props` для настройки путей сборки.

Все выходные файлы помещаются в `bin/{framework}/`.

### 👤 Авторы
PascalABC.NET Compiler Team
 


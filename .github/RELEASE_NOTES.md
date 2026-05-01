## 下载说明

### Catalytic 主程序

| 文件 | 平台 |
|------|------|
| `Catalytic-arm64.dmg` | macOS（Apple Silicon） |
| `Catalytic-x64.dmg` | macOS（Intel） |
| `Catalytic-arm64.AppImage` | Linux ARM64 |
| `Catalytic-x64.AppImage` | Linux x64 |
| `Catalytic-arm64.zip` | Windows ARM64 |
| `Catalytic-x64.zip` | Windows x64 |

### 插件

> [!NOTE]
> **Catalytic 工作目录**是第一次启动主程序时让你选择的那个目录，后续所有配置、插件、数据都存放在里面。

> [!CAUTION]
> **示例插件仅供参考，请勿在生产环境中使用**
> 
> 本仓库中的插件均为样板代码，用于演示 插件 的使用方式。提供下载的唯一目的是让你能在主程序中看到插件加载后的实际界面效果。
> 
> 其中协调器插件会在程序启动 30 秒后自动触发测试流程，由于你没有配套的模拟环境，**运行后不会得到任何有意义的结果**。
> 
> 如需了解实现细节，请查阅 SDK 仓库：https://github.com/lzdev42/CatalyticKit

下载插件 zip 后解压，将解压出的**整个文件夹**放入 Catalytic 工作目录的 `plugins/` 目录下：

```
plugins/
├── CatalyticSerialPort/
│   ├── CatalyticSerialPort.dll
│   └── manifest.json
├── CsvReporter/
│   ├── CsvReporter.dll
│   └── manifest.json
├── SocketClient/
│   ├── SocketClient.dll
│   └── manifest.json
└── RemoteController/
    ├── RemoteController.dll
    └── manifest.json
```

| 插件 | 说明 |
|------|------|
| `CatalyticSerialPort` | 串口通信插件 |
| `CsvReporter` | CSV 数据导出插件 |
| `SocketClient` | Socket 客户端插件 |
| `RemoteController` | 远程控制插件，协调器 |

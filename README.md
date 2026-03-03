<h1 align="center">SmartNet AI Monitor</h1>

<p align="center">
  <strong>An advanced, completely offline AI-driven network diagnostic suite for Windows.</strong> 
  Designed with cutting-edge .NET 8, WPF, and Microsoft ONNX runtime, this lightweight application grants total visibility into local Wi-Fi and Ethernet networks.
</p>

<p align="center">
  <img src="Assets/app_icon.png" width="150" alt="SmartNet AI Monitor Core Identity Icon"/>
</p>

---

## 🌟 Features Overview

- **🧠 ONNX Accelerated AI Threat Engine:** Utilizes the local Microsoft ML.NET/ONNX framework to detect high-frequency port scraping, suspicious exfiltration patterns, and potential data leaks in real-time, operating 100% offline without uploading your packets to the cloud.
- **🌐 Deep Packet Analysis (SharpPcap):** WireShark-style packet tracing optimized into a sleek hardware-accelerated DataGrid, offering instant syntax highlighting for TCP, UDP, DNS, and HTTP/S traffic.
- **📡 Automatic Device Discovery:** Rapid subnet sweeps utilizing ARP and ICMP broadcast, instantly identifying connected phones, IoT devices, laptops, and routers alongside real-time live ping response charts.
- **🗺️ Interactive Topology Map:** Real-time geometric visualizer mapping the relationship between your gateway and connected nodes, complete with interactive drag-and-drop and zoom mechanics built natively in WPF.
- **🛠️ Integrated Pro-Tools Module:**
  - **Bandwidth Speed Test:** Verifies true Internet throughput against public Cloudflare servers.
  - **Wake-On-LAN (WOL):** Remotely boot sleeping devices directly from the internal dashboard map.
  - **IP Geolocation:** Trace packets to their physical global location instantly.
  - **CSV Data Export:** Compile PDF or Excel compatible reports.
- **🔋 Zero Cloud / Privacy Built-in:** All logging and historical configurations are securely stored inside a localized SQLite instance on your hard drive. 
- **🖥️ Hardware Accelerated "Cyber Dark" UI:** Optimized vector icons, beautiful gradient designs, and dark/light mode toggles.

## 🛠️ Tech Stack & Architecture

This application was engineered targeting modern efficiency.
- **Framework:** .NET 8 C# (WPF) Native compiled for `win-x64`, `win-x86`, and `win-arm64`.
- **UI System:** [WPF UI (Fluent Design System)](https://github.com/lepoco/wpfui) & Custom Control Logic
- **Charting Engine:** [ScottPlot 5](https://scottplot.net/)
- **Packet Sniffing:** [SharpPcap](https://github.com/dotpcap/sharppcap) & PacketDotNet (requires Npcap driver)
- **Machine Learning Layer:** Microsoft.ML.OnnxRuntime
- **Persistence Layer:** Microsoft.Data.Sqlite 

## 🚀 Building from Source

To compile and package SmartNet AI Monitor for yourself:

1. Clone the repository to your local Windows environment.
2. Install the **.NET 8 SDK** (Specifically targetting SDK `10.0.102` or later).
3. Ensure the underlying machine compiling the binaries has **C++ Desktop Development** and **Windows 10 SDK (Minimum 10.0.17763.0)** workloads installed in Visual Studio.
4. Run the restore sequence to generate all NuGet bindings:
   ```powershell
   dotnet restore
   ```
5. To execute the application natively with JIT output:
   ```powershell
   dotnet run
   ```



### Note on Npcap
In order to utilize the Advanced Packet Capture module, users must have the cross-platform `Npcap` loopback driver installed on their system (which is traditionally bundled with WireShark installations). 

## ⚖️ License
*(Your chosen open-source license goes here; e.g. MIT, GPL-3.0, Apache-2.0)*

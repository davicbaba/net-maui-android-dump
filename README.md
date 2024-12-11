# Android Dump Generation Issue in .NET MAUI Blazor Hybrid

This repository demonstrates a .NET MAUI Blazor Hybrid application that reproduces an issue when attempting to generate dumps on Android.

## Steps to Reproduce

1. Run the `AndroidDumpGeneration` project on an Android device or emulator.
2. Click the **Generate Dump** button on the home page.
3. The error will occur, and it is displayed on the screen.

## Error Message

```text
Microsoft.Diagnostics.NETCore.Client.ServerNotAvailableException: Unable to connect to Process 28258. Please verify that /data/user/0/com.companyname.androiddumpgeneration/cache/ is writable by the current user. If the target process has environment variable TMPDIR set, please set TMPDIR to the same directory. Please see https://aka.ms/dotnet-diagnostics-port for more information
   at Microsoft.Diagnostics.NETCore.Client.PidIpcEndpoint.GetDefaultAddress(Int32 pid)
   at Microsoft.Diagnostics.NETCore.Client.PidIpcEndpoint.GetDefaultAddress()
   at Microsoft.Diagnostics.NETCore.Client.PidIpcEndpoint.ConnectAsync(CancellationToken token)
   at Microsoft.Diagnostics.NETCore.Client.IpcClient.SendMessageGetContinuationAsync(IpcEndpoint endpoint, IpcMessage message, CancellationToken cancellationToken)
   at Microsoft.Diagnostics.NETCore.Client.IpcClient.SendMessageAsync(IpcEndpoint endpoint, IpcMessage message, CancellationToken cancellationToken)
   at Microsoft.Diagnostics.NETCore.Client.DiagnosticsClient.WriteDumpAsync(DumpType dumpType, String dumpPath, WriteDumpFlags flags, CancellationToken token)
   at AndroidDumpGeneration.Components.Pages.Home.WriteDumpAsync() in C:\Users\davic\OneDrive\Documentos\GitRepositories\net-maui-android-dump\AndroidDumpGeneration\Components\Pages\Home.razor:line 49
   at AndroidDumpGeneration.Components.Pages.Home.GenerateDumpAsync() in C:\Users\davic\OneDrive\Documentos\GitRepositories\net-maui-android-dump\AndroidDumpGeneration\Components\Pages\Home.razor:line 25
```



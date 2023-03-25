# Readme

This repository seeks to demonstrate an unexpected effect when Consuming the [Ultz.Native.GLFW](https://www.nuget.org/packages/Ultz.Native.GLFW/) nuget package.  
It contains two Console applications targeting .Net7 and .Net 4.6.1 respectively and consuming aforementioned package.  
  
When building the `net7` project, the nuget package will automatically add a `runtimes` folder containing all relevant native glfw3 libraries to its output puth.  

On the other hand, when building the `net461` project, nothing will be added to its output directory while the nuget package contents suggest, that the original intent was to [copy a platform specific library binary to its output directory](https://github.com/dotnet/Silk.NET/blob/main/src/Native/Silk.NET.SDL.Native/build/net461/Ultz.Native.SDL.props).
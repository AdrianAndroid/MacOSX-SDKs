MacOSX-SDKs
---
**10.1.5 - 11.3**

A collection of those pesky SDK folders.  Compiled from various releases of Xcode.

If you don't need this entire repository, each SDK is available [here](https://github.com/phracker/MacOSX-SDKs/releases).


<sub>Outdated versions: **[mediafire](http://www.mediafire.com/?a4g384ysgy5rg)** /  **[mega.co.nz](https://mega.co.nz/#F!H8xGhaDD!Uv5BTPr0LP7IU5pj0WGCKg)** / 
**[mediafire](http://www.mediafire.com/?abr89fy4uaz3z)** /  **[mega.co.nz](https://mega.co.nz/#F!4U4SXAxa!ZVltflL2O_5q57R0BVsPTg)**.
</sub>

**Important**

Modern versions of Xcode (7.3+) need you to edit the `MinimumSDKVersion` in this file to use older SDKs:
`/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Info.plist`

**Usage**

Set the SDKROOT environment variable:
```
export SDKROOT=path-to-old-sdk
```

If you put an old SDK in a nonstandard path, Apple's hacks in /usr/bin which redirect to calling Apple's
tools in the XCode installation may fail. If your build system fails to find the compiler, explicitly
specify its path:

```
export CC="/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/clang"
export CXX="/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/clang++"
```

If you are building a project with CMake, using the default Unix Makefile generator may fail to
find the real `make` binary even if you put it in your $PATH before /usr/bin. To hack around this, install
[Ninja](https://ninja-build.org/) in your $PATH and use the Ninja CMake generator by running your CMake
configure step with:

```
cmake -G Ninja -S project-root-dir -B build-output-dir
```

alias use-MacOSX='sudo ln -snf /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.1.5='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.1.5.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.10='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.10.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.11='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.11.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.12='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.12.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.13='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.13.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.14='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.14.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.15='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.15.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.2.8='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.2.8.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.3.0='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.3.0.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.3.9='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.3.9.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.4u='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.4u.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.5='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.5.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.6='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.6.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.7='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.7.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.8='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.8.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX10.9='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX10.9.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX11.0='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX11.0.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX11.1='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX11.1.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
alias use-MacOSX11.3='sudo ln -snf /Users/zhaojian/bin/MacOSX-SDKs/MacOSX11.3.sdk /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX12.3.sdk'
\# echo 'MacOSSK:use-MacOSX10.1.5/use-MacOSX10.10/use-MacOSX10.11/use-MacOSX10.12/use-MacOSX10.13/use-MacOSX10.14/use-MacOSX10.15/use-MacOSX10.2.8/use-MacOSX10.3.0/use-MacOSX10.3.9/use-MacOSX10.4u/use-MacOSX10.5/use-MacOSX10.6/use-MacOSX10.7/use-MacOSX10.8/use-MacOSX10.9/use-MacOSX11.0/use-MacOSX11.1/use-MacOSX11.3'
\# echo 'MacOSSK:'
alias print-use-MacOSX="printUseMacOSX(){ echo 'use-MacOSX10.1.5\tuse-MacOSX10.10\tuse-MacOSX10.11\tuse-MacOSX10.12'; echo 'use-MacOSX10.13\tuse-MacOSX10.14\tuse-MacOSX10.15\tuse-MacOSX10.2.8'; echo 'use-MacOSX10.3.0\tuse-MacOSX10.3.9\tuse-MacOSX10.4u\tuse-MacOSX10.5'; echo 'use-MacOSX10.6\tuse-MacOSX10.7\tuse-MacOSX10.8\tuse-MacOSX10.9'; echo 'use-MacOSX11.0\tuse-MacOSX11.1\tuse-MacOSX11.3'; };printUseMacOSX" 
echo 'MacOSSK: print-use-MacOSX'


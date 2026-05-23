### 1.2.5 (unreleased)

- added CPPIA script breakpoint support (deferred registration when scripts load; hxcpp 4.x via `__hxcpp_dbg_setOnScriptLoadedFunction`, Haxe 5 via `generateFilePathMaps()` on script load — requires hxcpp with ungated script-loaded callback)
- CPPIA source roots resolve relative to executable dir; optional `HXCPP_CPPIA_SOURCE_ROOTS` env
- warn once when CPPIA scripts use relative source paths (Haxe 5 emits absolute debug paths by default)
- launch configs accept `args`, `cwd`, and `env` (merged into the spawned debuggee process)
- fixed debugger initialization order to match the Debug Adapter Protocol ([#24](https://github.com/vshaxe/hxcpp-debugger/issues/24))
- fixed UTF-8 handling in debug server socket writes ([#31](https://github.com/vshaxe/hxcpp-debugger/issues/31))
- fixed compilation with Haxe 5 ([#41](https://github.com/vshaxe/hxcpp-debugger/issues/41))
- fixed debug server macro injection with Haxe 5 ([#40](https://github.com/vshaxe/hxcpp-debugger/issues/40))
- fixed deprecation warnings with Haxe 4.2+ ([#28](https://github.com/vshaxe/hxcpp-debugger/issues/28))
- fixed `@:enum` abstract deprecation warnings in the debug server
- fixed launch config schema types (`bool` → `boolean`) ([#25](https://github.com/vshaxe/hxcpp-debugger/issues/25))
- require VS Code 1.75+ (removed redundant `activationEvents`)

### 1.2.4 (April 11, 2019)

- fixed removal of breakpoints

### 1.2.3 (April 2, 2019)

- fixed a crash on Windows when continuing from a breakpoint
- fixed an issue with class instance printing with NME / Lime legacy
- fixed inspection of static properties
- fixed a deadlock when getting variables

### 1.2.2 (March 23, 2019)

- fixed deprecation warnings with Haxe 4.0.0-rc.2 
- fixed debugger not stopping on last line of `main()` ([#18](https://github.com/vshaxe/hxcpp-debugger/issues/18))

### 1.2.1 (February 21, 2019)

- fixed default registrations for watch / conditional breakpoints ([#17](https://github.com/vshaxe/hxcpp-debugger/issues/17))

### 1.2.0 (February 20, 2019)

- added some support for statics in watch / conditional breakpoints ([#17](https://github.com/vshaxe/hxcpp-debugger/issues/17))
- fixed hxcpp-debug-server setup with spaces in username
- fixed "Start Debugging" not doing anything without a `launch.json`
- updated `${workspaceRoot}` to `${workspaceFolder}`

### 1.1.1 (November 10, 2018)

- fixed compilation with `-D hscriptPos` ([#14](https://github.com/vshaxe/hxcpp-debugger/issues/14))

### 1.1.0 (October 17, 2018)

- added support for attach requests ([#1](https://github.com/vshaxe/hxcpp-debugger/issues/1))
- added support for watching expressions ([#2](https://github.com/vshaxe/hxcpp-debugger/issues/2))
- added support for conditional breakpoints ([#12](https://github.com/vshaxe/hxcpp-debugger/issues/12))
- compatibility fixes for VSCode 1.28

### 1.0.0 (July 5, 2018)

- initial release
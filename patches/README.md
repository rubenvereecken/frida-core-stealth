# frida-core Stealth Patches

Patches to evade common Frida detection methods.

See the [main repository README](../../../README.md#option-2-manual-patching-for-maintainers) for instructions on how to apply these patches.

## Available Patches

| Patch                                                                              | Description                                                                                |
| ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| [001-obfuscate-threads.patch](./001-obfuscate-threads.patch)                       | Obfuscate thread names from "frida-_" to "banana-_" to avoid string-based detection        |
| [002-obfuscate-rpc.patch](./002-obfuscate-rpc.patch)                               | Obfuscate RPC protocol identifier "frida:rpc" using Base64 encoding                        |
| [003-obfuscate-network.patch](./003-obfuscate-network.patch)                       | Change default ports (27042→27043, 27052→27053) and bind address (127.0.0.1→0.0.0.0)       |
| [004-obfuscate-branding.patch](./004-obfuscate-branding.patch)                     | Replace Frida branding with Banana in headers, identifiers, and log domain                 |
| [005-obfuscate-selinux.patch](./005-obfuscate-selinux.patch)                       | Obfuscate SELinux contexts from "frida_file"/"frida_memfd" to "banana_file"/"banana_memfd" |
| [006-obfuscate-socket-paths.patch](./006-obfuscate-socket-paths.patch)             | Obfuscate socket/IPC paths from "frida:" to "banana:" and "/frida-" to "/banana-"          |
| [007-obfuscate-server-identifiers.patch](./007-obfuscate-server-identifiers.patch) | Randomize server GUID and temporary directory name to prevent fingerprinting               |
| [008-obfuscate-entrypoint.patch](./008-obfuscate-entrypoint.patch)                 | Obfuscate entry point symbol from "frida_agent_main" to "banana_main"                      |
| [009-randomize-agent-filename.patch](./009-randomize-agent-filename.patch)         | Randomize agent library filename from "frida-agent-*.so" to "{random}-*.so"                |

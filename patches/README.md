# frida-core Stealth Patches

Patches to evade common Frida detection methods.

See the [main repository README](../../../README.md#option-2-manual-patching-for-maintainers) for instructions on how to apply these patches.

## Available Patches

| Patch                                                        | Description                                                                         |
| ------------------------------------------------------------ | ----------------------------------------------------------------------------------- |
| [001-obfuscate-threads.patch](./001-obfuscate-threads.patch) | Obfuscate thread names from "frida-_" to "banana-_" to avoid string-based detection |
| [002-obfuscate-rpc.patch](./002-obfuscate-rpc.patch)         | Obfuscate RPC protocol identifier "frida:rpc" using Base64 encoding                |

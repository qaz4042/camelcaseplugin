# CamelCaseFix

`CamelCaseFix` is a community-maintained fork of the original CamelCase plugin
for IntelliJ IDEs. It fixes the missing `WordUtils` dependency on modern IDEs.

Switch easily between kebab-case, SNAKE_CASE, PascalCase, camelCase, snake_case or space case. See Edit menu or use ⇧ + ⌥ + U / Shift + Alt + U.

Allows to disable some conversions or change their order in the preferences.

Source and issue tracker: https://github.com/qaz4042/camelcaseplugin

Please see the original example for a demonstration:

![Demonstration](https://github.com/user-attachments/assets/72001e9b-402d-4971-8a82-3375c70d858d)

## Install

Install `CamelCaseFix` from the JetBrains Marketplace when it is approved, or
use the ZIP produced by the build below through **Settings → Plugins → Install
Plugin from Disk…**.

## Build from source

The repository produces a complete Marketplace-style plugin ZIP from source:

```sh
./gradlew buildPlugin
```

With an installed IntelliJ IDEA, avoid downloading the platform distribution:

```sh
LOCAL_IDE_PATH="/Applications/IntelliJ IDEA.app/Contents" ./gradlew buildPlugin
```

The output is under `build/distributions/`. The build targets IntelliJ platform
build 262 and later, which includes IntelliJ IDEA 2026.2.

For the original plugin's binary-compatible 3.0.12 hotfix, the repository also
contains `scripts/build-local.py`. It is kept for rollback and upstream debugging;
the Marketplace artifact should be built with `./gradlew buildPlugin`.

The independent plugin output is `build/distributions/camelcasefix-1.0.0.zip`.
Install it via **Settings → Plugins → ⚙ → Install Plugin from Disk…**, then restart.
The plugin ID is `io.github.qaz4042.camelcasefix`, so it can be installed beside
the original CamelCase plugin while both are being compared.

The original project is MIT-licensed; this fork retains that license and credits
the upstream project.

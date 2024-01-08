# RARS

RARS, the RISC-V Assembler, Simulator, and Runtime, will assemble and simulate the execution of RISC-V assembly language programs. Its primary goal is to be an effective development environment for people getting started with RISC-V.

Original repo: [rars](https://github.com/TheThirdOne/rars)

In case it becomes unavailable, here's a fork: [rars](https://github.com/andrewt0301/rars)

RARS made into macOS app using ``jpackage`` on original RARS jar distribution:

```bash
jpackage --input src --main-jar rars.jar \
  -n RARS --main-class rars.Launch \
  --app-version 1.6 \
  --icon ./RARS.icns \
  --mac-package-identifier "RARS" \
  --mac-package-name "RARS" \
  --mac-app-category "public.app-category.developer" \
  --java-options "-Djpackage.app-version=1.6.0 \
    -Dapple.laf.useScreenMenuBar=true \
    -Duser.dir=/Contents -Xdock:name=RARS \
    -Dcom.apple.smallTabs=true \
    -Dapple.awt.application.name=RARS \
    -Dcom.apple.macos.useScreenMenuBar=true \
    -Dcom.apple.macos.use-file-dialog-packages=true" \
  --runtime-image #<JRE distribution path. I used AZUL OpenJDK Builds: https://www.azul.com/downloads/#zulu>
```

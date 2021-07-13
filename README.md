# New Bug [fixed - see `build.rs`]
Can't transpile `actix-web` VIA `cargo build --release --target=x86_64-unknown-linux-musl`
```
➜  actix-web-bug-2020-7-13 git:(main) ./build.sh
   Compiling ring v0.16.20
   Compiling brotli-sys v0.3.2
   Compiling unicode-normalization v0.1.19
   Compiling quote v1.0.9
   Compiling iovec v0.1.4
   Compiling net2 v0.2.37
   Compiling signal-hook-registry v1.4.0
   Compiling num_cpus v1.13.0
error: failed to run custom build command for `brotli-sys v0.3.2`

Caused by:
  process didn't exit successfully: `/Users/colbyn/Scratch/actix-web-bug-2020-7-13/target/release/build/brotli-sys-c7b71fef0074ab07/build-script-build` (exit code: 1)
  --- stdout
  cargo:include=/Users/colbyn/.cargo/registry/src/github.com-1ecc6299db9ec823/brotli-sys-0.3.2/brotli/include
  TARGET = Some("x86_64-unknown-linux-musl")
  OPT_LEVEL = Some("3")
  HOST = Some("x86_64-apple-darwin")
  CC_x86_64-unknown-linux-musl = None
  CC_x86_64_unknown_linux_musl = None
  TARGET_CC = None
  CC = None
  CROSS_COMPILE = None
  CFLAGS_x86_64-unknown-linux-musl = None
  CFLAGS_x86_64_unknown_linux_musl = None
  TARGET_CFLAGS = None
  CFLAGS = None
  CRATE_CC_NO_DEFAULTS = None
  DEBUG = Some("false")
  CARGO_CFG_TARGET_FEATURE = Some("fxsr,sse,sse2")
  running: "musl-gcc" "-O3" "-ffunction-sections" "-fdata-sections" "-fPIC" "-m64" "-I" "brotli/include" "-o" "/Users/colbyn/Scratch/actix-web-bug-2020-7-13/target/x86_64-unknown-linux-musl/release/build/brotli-sys-fbf7e23b3c7ec250/out/brotli/common/dictionary.o" "-c" "brotli/common/dictionary.c"

  --- stderr
  fatal: not a git repository (or any of the parent directories): .git


  error occurred: Failed to find tool. Is `musl-gcc` installed?


warning: build failed, waiting for other jobs to finish...
error: build failed
```

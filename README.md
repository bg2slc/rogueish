# rogueish
Traditional roguelike based on the tutorial at https://tomassedovic.github.io/roguelike-tutorial/part-1-graphics.html

*Abandoned* due to the fact that tcod is an older library. It doesn't seem to play well with 2021 edition of rust. I may come back to this if I figure out how to do error handling for this particular problem. I did this as part of a tutorial to help me learn rust, but trying to solve the issue is beyond my abilities at the moment. As far as I can tell, it's something to do with the way tcod handles keyboard or mouse input. Output as follows:

➜  cargo run RUST_BACKTRACE=1                                            (main|●💩) 00:41
    Finished dev [unoptimized + debuginfo] target(s) in 0.00s
     Running `target/debug/rogueish RUST_BACKTRACE=1`
24 bits font.
key color : 0 0 0
24bits greyscale font. converting to 32bits
thread 'main' panicked at 'attempted to leave type `tcod_sys::TCOD_key_t` uninitialized, which is invalid', /home/bgarrett/.cargo/registry/src/github.com-1ecc6299db9ec823/tcod-0.15.0/src/input.rs:193:53
stack backtrace:
   0: rust_begin_unwind
             at /rustc/fe5b13d681f25ee6474be29d748c65adcd91f69e/library/std/src/panicking.rs:584:5
   1: core::panicking::panic_fmt
             at /rustc/fe5b13d681f25ee6474be29d748c65adcd91f69e/library/core/src/panicking.rs:143:14
   2: core::panicking::panic
             at /rustc/fe5b13d681f25ee6474be29d748c65adcd91f69e/library/core/src/panicking.rs:48:5
   3: core::mem::uninitialized
             at /rustc/fe5b13d681f25ee6474be29d748c65adcd91f69e/library/core/src/mem/mod.rs:679:9
   4: tcod::input::check_for_event
             at /home/bgarrett/.cargo/registry/src/github.com-1ecc6299db9ec823/tcod-0.15.0/src/input.rs:193:53
   5: rogueish::main
             at ./src/main.rs:788:15
   6: core::ops::function::FnOnce::call_once
             at /rustc/fe5b13d681f25ee6474be29d748c65adcd91f69e/library/core/src/ops/function.rs:227:5


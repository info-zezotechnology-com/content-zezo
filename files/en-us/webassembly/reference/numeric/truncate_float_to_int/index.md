---
title: Truncate (float to int)
slug: WebAssembly/Reference/Numeric/Truncate_float_to_int
page-type: webassembly-instruction
sidebar: webassemblysidebar
---

The **`trunc`** instructions, are used for converting floating points to integers. It's named truncate since it truncates the fractional part of the number when doing the conversion. There are signed and unsigned versions of this instruction.

There's another [**`trunc`**](/en-US/docs/WebAssembly/Reference/Numeric/Truncate_float_to_float) instruction that truncates the fractional part of a floating point without converting it to and integer.

{{InteractiveExample("Wat Demo: trunc_float_to_int", "tabbed-taller")}}

```wat interactive-example
(module
  (import "console" "log" (func $log (param i32)))
  (func $main

    f32.const 10.5 ;; push an f32 onto the stack

    i32.trunc_f32_s ;; convert from f32 to signed i32 rounding towards zero (.5 will be lost)

    call $log ;; log the result

  )
  (start $main)
)
```

```js interactive-example
const url = "{%wasm-url%}";
await WebAssembly.instantiateStreaming(fetch(url), { console });
```

## Syntax

```wat
;; push an f32 onto the stack
f32.const 10.5

;; convert from f32 to signed i32 rounding towards zero (.5 will be lost)
i32.trunc_f32_s

;; the top item on the stack will now be the value 10 of type f32
```

| Instruction       | Binary opcode |
| ----------------- | ------------- |
| `i32.trunc_f32_s` | `0xa8`        |
| `i32.trunc_f32_u` | `0xa9`        |
| `i32.trunc_f64_s` | `0xaa`        |
| `i32.trunc_f64_u` | `0xab`        |
| `i64.trunc_f32_s` | `0xae`        |
| `i64.trunc_f32_u` | `0xaf`        |
| `i64.trunc_f64_s` | `0xb0`        |
| `i64.trunc_f64_u` | `0xb1`        |

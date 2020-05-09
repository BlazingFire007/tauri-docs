---
title: "trait.ResultExt"
---

Trait [tauri\\\_utils](/docs/api/rust/tauri\_utils/index.html)::[ResultExt](/docs/api/rust/tauri\_utils/)
=========================================================================================================

```rust
pub trait ResultExt&lt;T&gt; {
    fn [chain\\\_err](/docs/api/rust/tauri\_utils/about:blank#tymethod.chain\_err)&lt;F, EK&gt;(self, callback: F) -&gt; [Result](https://doc.rust-lang.org/nightly/core/result/enum.Result.html "enum core::result::Result")&lt;T, [Error](/docs/api/rust/tauri\_utils/../tauri\_utils/struct.Error.html "struct tauri\_utils::Error")\&gt;&lt;br/&gt;    where&lt;br/&gt;        F: [FnOnce](https://doc.rust-lang.org/nightly/core/ops/function/trait.FnOnce.html "trait core::ops::function::FnOnce")() -&gt; EK,&lt;br/&gt;        EK: [Into](https://doc.rust-lang.org/nightly/core/convert/trait.Into.html "trait core::convert::Into")&lt;[ErrorKind](/docs/api/rust/tauri\_utils/../tauri\_utils/enum.ErrorKind.html "enum tauri\_utils::ErrorKind")\&gt;;
}
```

Additional methods for <span>Result</span>, for easy interaction with this crate.

Required methods
----------------

### <span>fn [chain\_err](/docs/api/rust/tauri\_utils/about:blank#tymethod.chain\_err)&lt;F, EK&gt;(self, callback: F) -&gt; [Result](https://doc.rust-lang.org/nightly/core/result/enum.Result.html "enum core::result::Result")&lt;T, [Error](/docs/api/rust/tauri\_utils/../tauri\_utils/struct.Error.html "struct tauri\_utils::Error")&gt; where&lt;br/&gt;    F: [FnOnce](https://doc.rust-lang.org/nightly/core/ops/function/trait.FnOnce.html "trait core::ops::function::FnOnce")() -&gt; EK,&lt;br/&gt;    EK: [Into](https://doc.rust-lang.org/nightly/core/convert/trait.Into.html "trait core::convert::Into")&lt;[ErrorKind](/docs/api/rust/tauri\_utils/../tauri\_utils/enum.ErrorKind.html "enum tauri\_utils::ErrorKind")&gt;,</span> 

If the <span>Result</span> is an <span>Err</span> then <span>chain\_err</span> evaluates the closure, which returns &lt;em&gt;some type that can be converted to <span>ErrorKind</span>&lt;/em&gt;, boxes the original error to store as the cause, then returns a new error containing the original error.

Loading content...

Implementations on Foreign Types
--------------------------------

### <span>impl&lt;T, E&gt; [ResultExt](/docs/api/rust/tauri\_utils/../tauri\_utils/trait.ResultExt.html "trait tauri\_utils::ResultExt")&lt;T&gt; for [Result](https://doc.rust-lang.org/nightly/core/result/enum.Result.html "enum core::result::Result")&lt;T, E&gt; where&lt;br/&gt;    E: [Error](https://doc.rust-lang.org/nightly/std/error/trait.Error.html "trait std::error::Error") + [Send](https://doc.rust-lang.org/nightly/core/marker/trait.Send.html "trait core::marker::Send") + 'static,</span> 

#### <span>fn [chain\_err](/docs/api/rust/tauri\_utils/about:blank#method.chain\_err)&lt;F, EK&gt;(self, callback: F) -&gt; [Result](https://doc.rust-lang.org/nightly/core/result/enum.Result.html "enum core::result::Result")&lt;T, [Error](/docs/api/rust/tauri\_utils/../tauri\_utils/struct.Error.html "struct tauri\_utils::Error")&gt; where&lt;br/&gt;    F: [FnOnce](https://doc.rust-lang.org/nightly/core/ops/function/trait.FnOnce.html "trait core::ops::function::FnOnce")() -&gt; EK,&lt;br/&gt;    EK: [Into](https://doc.rust-lang.org/nightly/core/convert/trait.Into.html "trait core::convert::Into")&lt;[ErrorKind](/docs/api/rust/tauri\_utils/../tauri\_utils/enum.ErrorKind.html "enum tauri\_utils::ErrorKind")&gt;,</span> 

### <span>impl&lt;T&gt; [ResultExt](/docs/api/rust/tauri\_utils/../tauri\_utils/trait.ResultExt.html "trait tauri\_utils::ResultExt")&lt;T&gt; for [Option](https://doc.rust-lang.org/nightly/core/option/enum.Option.html "enum core::option::Option")&lt;T&gt;</span>

#### <span>fn [chain\_err](/docs/api/rust/tauri\_utils/about:blank#method.chain\_err)&lt;F, EK&gt;(self, callback: F) -&gt; [Result](https://doc.rust-lang.org/nightly/core/result/enum.Result.html "enum core::result::Result")&lt;T, [Error](/docs/api/rust/tauri\_utils/../tauri\_utils/struct.Error.html "struct tauri\_utils::Error")&gt; where&lt;br/&gt;    F: [FnOnce](https://doc.rust-lang.org/nightly/core/ops/function/trait.FnOnce.html "trait core::ops::function::FnOnce")() -&gt; EK,&lt;br/&gt;    EK: [Into](https://doc.rust-lang.org/nightly/core/convert/trait.Into.html "trait core::convert::Into")&lt;[ErrorKind](/docs/api/rust/tauri\_utils/../tauri\_utils/enum.ErrorKind.html "enum tauri\_utils::ErrorKind")&gt;,</span> 

Loading content...

Implementors
------------

Loading content...window.inlined\\\_types=new Set(\[\]);
      
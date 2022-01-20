---
title: Struct tauri::api::file::Move
sidebar_label: struct.Move
custom_edit_url: null
---

  # Struct tauri::api::file::Move,

```rs
pub struct Move<'a> { /* fields omitted */ }
```

Expand description

Moves a file from the given path to the specified destination.

`source` and `dest` must be on the same filesystem. If `replace_using_temp` is specified, the destination file will be replaced using the given temporary path.

-   Errors:

    -   Io - copying / renaming

## Implementations

### impl&lt;'a> [Move](/docs/api/rust/tauri/struct.Move "struct tauri::api::file::Move")&lt;'a>[\[src\]](/docs/api/rust/tauri/../../../src/tauri/api/file/file_move.rs#21-89 "goto source code")

#### pub fn [from_source](/docs/api/rust/tauri/about:blank#method.from_source)(source: &'a [Path](https://doc.rust-lang.org/1.54.0/std/path/struct.Path.html "struct std::path::Path")) -> [Move](/docs/api/rust/tauri/struct.Move "struct tauri::api::file::Move")&lt;'a>[\[src\]](/docs/api/rust/tauri/../../../src/tauri/api/file/file_move.rs#23-25 "goto source code")

Specify source file

#### pub fn [replace_using_temp](/docs/api/rust/tauri/about:blank#method.replace_using_temp)(&mut self, temp: &'a [Path](https://doc.rust-lang.org/1.54.0/std/path/struct.Path.html "struct std::path::Path")) -> [&mut](https://doc.rust-lang.org/1.54.0/std/primitive.reference.html)Self[\[src\]](/docs/api/rust/tauri/../../../src/tauri/api/file/file_move.rs#36-39 "goto source code")

If specified and the destination file already exists, the “destination” file will be moved to the given temporary location before the “source” file is moved to the “destination” file.

In the event of an `io` error while renaming “source” to “destination”, the temporary file will be moved back to “destination”.

The `temp` dir must be explicitly provided since `rename` operations require files to live on the same filesystem.

#### pub fn [to_dest](/docs/api/rust/tauri/about:blank#method.to_dest)(&self, dest: &[Path](https://doc.rust-lang.org/1.54.0/std/path/struct.Path.html "struct std::path::Path")) -> [Result](/docs/api/rust/tauri/../type.Result "type tauri::api::Result")&lt;[()](https://doc.rust-lang.org/1.54.0/std/primitive.unit.html)>[\[src\]](/docs/api/rust/tauri/../../../src/tauri/api/file/file_move.rs#42-60 "goto source code")

Move source file to specified destination (replace whole directory)

#### pub fn [walk_to_dest](/docs/api/rust/tauri/about:blank#method.walk_to_dest)(&self, dest: &[Path](https://doc.rust-lang.org/1.54.0/std/path/struct.Path.html "struct std::path::Path")) -> [Result](/docs/api/rust/tauri/../type.Result "type tauri::api::Result")&lt;[()](https://doc.rust-lang.org/1.54.0/std/primitive.unit.html)>[\[src\]](/docs/api/rust/tauri/../../../src/tauri/api/file/file_move.rs#64-88 "goto source code")

Walk in the source and copy all files and create directories if needed by replacing existing elements. (equivalent to a cp -R)

## Trait Implementations

### impl&lt;'a> [Debug](https://doc.rust-lang.org/1.54.0/core/fmt/trait.Debug.html "trait core::fmt::Debug") for [Move](/docs/api/rust/tauri/struct.Move "struct tauri::api::file::Move")&lt;'a>[\[src\]](/docs/api/rust/tauri/../../../src/tauri/api/file/file_move.rs#16 "goto source code")

#### fn [fmt](https://doc.rust-lang.org/1.54.0/core/fmt/trait.Debug.html#tymethod.fmt)(&self, f: &mut [Formatter](https://doc.rust-lang.org/1.54.0/core/fmt/struct.Formatter.html "struct core::fmt::Formatter")&lt;'\_>) -> [Result](https://doc.rust-lang.org/1.54.0/core/fmt/type.Result.html "type core::fmt::Result")[\[src\]](/docs/api/rust/tauri/../../../src/tauri/api/file/file_move.rs#16 "goto source code")

Formats the value using the given formatter. [Read more](https://doc.rust-lang.org/1.54.0/core/fmt/trait.Debug.html#tymethod.fmt)

## Auto Trait Implementations

### impl&lt;'a> [RefUnwindSafe](https://doc.rust-lang.org/1.54.0/std/panic/trait.RefUnwindSafe.html "trait std::panic::RefUnwindSafe") for [Move](/docs/api/rust/tauri/struct.Move "struct tauri::api::file::Move")&lt;'a>

### impl&lt;'a> [Send](https://doc.rust-lang.org/1.54.0/core/marker/trait.Send.html "trait core::marker::Send") for [Move](/docs/api/rust/tauri/struct.Move "struct tauri::api::file::Move")&lt;'a>

### impl&lt;'a> [Sync](https://doc.rust-lang.org/1.54.0/core/marker/trait.Sync.html "trait core::marker::Sync") for [Move](/docs/api/rust/tauri/struct.Move "struct tauri::api::file::Move")&lt;'a>

### impl&lt;'a> [Unpin](https://doc.rust-lang.org/1.54.0/core/marker/trait.Unpin.html "trait core::marker::Unpin") for [Move](/docs/api/rust/tauri/struct.Move "struct tauri::api::file::Move")&lt;'a>

### impl&lt;'a> [UnwindSafe](https://doc.rust-lang.org/1.54.0/std/panic/trait.UnwindSafe.html "trait std::panic::UnwindSafe") for [Move](/docs/api/rust/tauri/struct.Move "struct tauri::api::file::Move")&lt;'a>

## Blanket Implementations

### impl&lt;T> [Any](https://doc.rust-lang.org/1.54.0/core/any/trait.Any.html "trait core::any::Any") for T where T: 'static + ?[Sized](https://doc.rust-lang.org/1.54.0/core/marker/trait.Sized.html "trait core::marker::Sized"),[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/any.rs.html#131-135 "goto source code")

#### pub fn [type_id](https://doc.rust-lang.org/1.54.0/core/any/trait.Any.html#tymethod.type_id)(&self) -> [TypeId](https://doc.rust-lang.org/1.54.0/core/any/struct.TypeId.html "struct core::any::TypeId")[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/any.rs.html#132 "goto source code")

Gets the `TypeId` of `self`. [Read more](https://doc.rust-lang.org/1.54.0/core/any/trait.Any.html#tymethod.type_id)

### impl&lt;T> [Borrow](https://doc.rust-lang.org/1.54.0/core/borrow/trait.Borrow.html "trait core::borrow::Borrow")&lt;T> for T where T: ?[Sized](https://doc.rust-lang.org/1.54.0/core/marker/trait.Sized.html "trait core::marker::Sized"),[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/borrow.rs.html#208-213 "goto source code")

#### pub fn [borrow](https://doc.rust-lang.org/1.54.0/core/borrow/trait.Borrow.html#tymethod.borrow)(&self) -> [&](https://doc.rust-lang.org/1.54.0/std/primitive.reference.html)T[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/borrow.rs.html#210 "goto source code")

Immutably borrows from an owned value. [Read more](https://doc.rust-lang.org/1.54.0/core/borrow/trait.Borrow.html#tymethod.borrow)

### impl&lt;T> [BorrowMut](https://doc.rust-lang.org/1.54.0/core/borrow/trait.BorrowMut.html "trait core::borrow::BorrowMut")&lt;T> for T where T: ?[Sized](https://doc.rust-lang.org/1.54.0/core/marker/trait.Sized.html "trait core::marker::Sized"),[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/borrow.rs.html#216-220 "goto source code")

#### pub fn [borrow_mut](https://doc.rust-lang.org/1.54.0/core/borrow/trait.BorrowMut.html#tymethod.borrow_mut)(&mut self) -> [&mut](https://doc.rust-lang.org/1.54.0/std/primitive.reference.html)T[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/borrow.rs.html#217 "goto source code")

Mutably borrows from an owned value. [Read more](https://doc.rust-lang.org/1.54.0/core/borrow/trait.BorrowMut.html#tymethod.borrow_mut)

### impl&lt;T> [From](https://doc.rust-lang.org/1.54.0/core/convert/trait.From.html "trait core::convert::From")&lt;T> for T[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/convert/mod.rs.html#544-548 "goto source code")

#### pub fn [from](https://doc.rust-lang.org/1.54.0/core/convert/trait.From.html#tymethod.from)(t: T) -> T[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/convert/mod.rs.html#545 "goto source code")

Performs the conversion.

### impl&lt;T, U> [Into](https://doc.rust-lang.org/1.54.0/core/convert/trait.Into.html "trait core::convert::Into")&lt;U> for T where U: [From](https://doc.rust-lang.org/1.54.0/core/convert/trait.From.html "trait core::convert::From")&lt;T>,[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/convert/mod.rs.html#533-540 "goto source code")

#### pub fn [into](https://doc.rust-lang.org/1.54.0/core/convert/trait.Into.html#tymethod.into)(self) -> U[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/convert/mod.rs.html#537 "goto source code")

Performs the conversion.

### impl&lt;T, U> [TryFrom](https://doc.rust-lang.org/1.54.0/core/convert/trait.TryFrom.html "trait core::convert::TryFrom")&lt;U> for T where U: [Into](https://doc.rust-lang.org/1.54.0/core/convert/trait.Into.html "trait core::convert::Into")&lt;T>,[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/convert/mod.rs.html#581-590 "goto source code")

#### type [Error](https://doc.rust-lang.org/1.54.0/core/convert/trait.TryFrom.html#associatedtype.Error) = [Infallible](https://doc.rust-lang.org/1.54.0/core/convert/enum.Infallible.html "enum core::convert::Infallible")

The type returned in the event of a conversion error.

#### pub fn [try_from](https://doc.rust-lang.org/1.54.0/core/convert/trait.TryFrom.html#tymethod.try_from)(value: U) -> [Result](https://doc.rust-lang.org/1.54.0/core/result/enum.Result.html "enum core::result::Result")&lt;T, &lt;T as [TryFrom](https://doc.rust-lang.org/1.54.0/core/convert/trait.TryFrom.html "trait core::convert::TryFrom")&lt;U>>::[Error](https://doc.rust-lang.org/1.54.0/core/convert/trait.TryFrom.html#associatedtype.Error "type core::convert::TryFrom::Error")>[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/convert/mod.rs.html#587 "goto source code")

Performs the conversion.

### impl&lt;T, U> [TryInto](https://doc.rust-lang.org/1.54.0/core/convert/trait.TryInto.html "trait core::convert::TryInto")&lt;U> for T where U: [TryFrom](https://doc.rust-lang.org/1.54.0/core/convert/trait.TryFrom.html "trait core::convert::TryFrom")&lt;T>,[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/convert/mod.rs.html#567-576 "goto source code")

#### type [Error](https://doc.rust-lang.org/1.54.0/core/convert/trait.TryInto.html#associatedtype.Error) = &lt;U as [TryFrom](https://doc.rust-lang.org/1.54.0/core/convert/trait.TryFrom.html "trait core::convert::TryFrom")&lt;T>>::[Error](https://doc.rust-lang.org/1.54.0/core/convert/trait.TryFrom.html#associatedtype.Error "type core::convert::TryFrom::Error")

The type returned in the event of a conversion error.

#### pub fn [try_into](https://doc.rust-lang.org/1.54.0/core/convert/trait.TryInto.html#tymethod.try_into)(self) -> [Result](https://doc.rust-lang.org/1.54.0/core/result/enum.Result.html "enum core::result::Result")&lt;U, &lt;U as [TryFrom](https://doc.rust-lang.org/1.54.0/core/convert/trait.TryFrom.html "trait core::convert::TryFrom")&lt;T>>::[Error](https://doc.rust-lang.org/1.54.0/core/convert/trait.TryFrom.html#associatedtype.Error "type core::convert::TryFrom::Error")>[\[src\]](https://doc.rust-lang.org/1.54.0/src/core/convert/mod.rs.html#573 "goto source code")

Performs the conversion.

### impl&lt;V, T> VZip&lt;V> for T where V: MultiLane&lt;T>,

#### pub fn [vzip](/docs/api/rust/tauri/about:blank#tymethod.vzip)(self) -> V
  
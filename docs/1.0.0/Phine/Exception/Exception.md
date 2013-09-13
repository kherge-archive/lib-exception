<small>Phine\Exception</small>

Exception
=========

Builds on the `Exception` class to add more features.

Signature
---------

- It is a(n) **class**.
- It is a subclass of [`Exception`](http://php.net/class.Exception).

Methods
-------

The class defines the following methods:

- [`createUsingFormat()`](#createUsingFormat) &mdash; Creates a new exception using a formatted message.
- [`createUsingLastError()`](#createUsingLastError) &mdash; Uses the last error message to create a new exception.

### `createUsingFormat()` <a name="createUsingFormat"></a>

Creates a new exception using a formatted message.

#### Description

A new exception is created after formatting the given arguments using
`vsprintf()`. If the last argument is an instance of the `Exception`
class, it will be used as the `$previous` exception in the new one
that is created.

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$format`
- It returns a(n) [`Exception`](../../Phine/Exception/Exception.md) value.

### `createUsingLastError()` <a name="createUsingLastError"></a>

Uses the last error message to create a new exception.

#### Description

A new exception will be created using the last error message, which is
returned by the `error_get_last()` function. If no error message was
generated, the `$default` message will be used. By default, that message
is &quot;(unknown error)&quot;.

The message `$prefix` will be added to any message that is used. The
prefix &quot;My prefix: &quot; with the error message &quot;my error&quot; will result in
&quot;My prefix: error message&quot; being used as the exception message.

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$prefix` (`string`) &mdash; The message prefix.
    - `$default` (`string`) &mdash; The default message.
- It returns a(n) [`Exception`](../../Phine/Exception/Exception.md) value.


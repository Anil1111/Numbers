## PeterO.Numbers.ERational

    public sealed class ERational :
        System.IComparable,
        System.IEquatable

Arbitrary-precision rational number. This class cannot be inherited.<b>Thread safety:</b>Instances of this class are immutable, so they are inherently safe for use by multiple threads. Multiple instances of this object with the same properties are interchangeable, so they should not be compared using the "==" operator (which only checks if each side of the operator is the same instance).

### ERational Constructor

    public ERational(
        PeterO.Numbers.EInteger numerator,
        PeterO.Numbers.EInteger denominator);

Initializes a new instance of the [PeterO.Numbers.ERational](PeterO.Numbers.ERational.md) class.

<b>Parameters:</b>

 * <i>numerator</i>: An arbitrary-precision integer.

 * <i>denominator</i>: Another arbitrary-precision integer.

<b>Exceptions:</b>

 * System.ArgumentNullException:
The parameter <i>numerator</i>
 or  <i>denominator</i>
 is null.

### NaN

    public static readonly PeterO.Numbers.ERational NaN;

A not-a-number value.

### NegativeInfinity

    public static readonly PeterO.Numbers.ERational NegativeInfinity;

Negative infinity, less than any other number.

### NegativeZero

    public static readonly PeterO.Numbers.ERational NegativeZero;

A rational number for negative zero.

### One

    public static readonly PeterO.Numbers.ERational One;

The rational number one.

### PositiveInfinity

    public static readonly PeterO.Numbers.ERational PositiveInfinity;

Positive infinity, greater than any other number.

### SignalingNaN

    public static readonly PeterO.Numbers.ERational SignalingNaN;

A signaling not-a-number value.

### Ten

    public static readonly PeterO.Numbers.ERational Ten;

The rational number ten.

### Zero

    public static readonly PeterO.Numbers.ERational Zero;

A rational number for zero.

### Denominator

    public PeterO.Numbers.EInteger Denominator { get; }

Gets this object's denominator.

<b>Returns:</b>

This object's denominator.

### IsFinite

    public bool IsFinite { get; }

Gets a value indicating whether this object is finite (not infinity or NaN).

<b>Returns:</b>

True if this object is finite (not infinity or NaN); otherwise, false.

### IsNegative

    public bool IsNegative { get; }

Gets a value indicating whether this object's value is negative (including negative zero).

<b>Returns:</b>

True if this object's value is negative; otherwise, false.

### IsZero

    public bool IsZero { get; }

Gets a value indicating whether this object's value equals 0.

<b>Returns:</b>

True if this object's value equals 0; otherwise, false.

### Numerator

    public PeterO.Numbers.EInteger Numerator { get; }

Gets this object's numerator.

<b>Returns:</b>

This object's numerator. If this object is a not-a-number value, returns the diagnostic information (which will be negative if this object is negative).

### Sign

    public int Sign { get; }

Gets the sign of this rational number.

<b>Returns:</b>

Zero if this value is zero or negative zero; -1 if this value is less than 0; and 1 if this value is greater than 0.

### UnsignedNumerator

    public PeterO.Numbers.EInteger UnsignedNumerator { get; }

Gets this object's numerator with the sign removed.

<b>Returns:</b>

This object's numerator. If this object is a not-a-number value, returns the diagnostic information.

### Abs

    public PeterO.Numbers.ERational Abs();

Not documented yet.

<b>Return Value:</b>

An arbitrary-precision rational number.

### Add

    public PeterO.Numbers.ERational Add(
        PeterO.Numbers.ERational otherValue);

Adds two rational numbers.

<b>Parameters:</b>

 * <i>otherValue</i>: Another arbitrary-precision rational number.

<b>Return Value:</b>

The sum of the two numbers. Returns not-a-number (NaN) if either operand is NaN.

<b>Exceptions:</b>

 * System.ArgumentNullException:
The parameter <i>otherValue</i>
 is null.

### CompareTo

    public sealed int CompareTo(
        PeterO.Numbers.ERational other);

Compares an arbitrary-precision rational number with this instance.

<b>Parameters:</b>

 * <i>other</i>: An arbitrary-precision rational number.

<b>Return Value:</b>

Zero if the values are equal; a negative number if this instance is less, or a positive number if this instance is greater.

### CompareToBinary

    public int CompareToBinary(
        PeterO.Numbers.EFloat other);

Compares an arbitrary-precision binary float with this instance.

<b>Parameters:</b>

 * <i>other</i>: An arbitrary-precision binary float.

<b>Return Value:</b>

Zero if the values are equal; a negative number if this instance is less, or a positive number if this instance is greater.

### CompareToDecimal

    public int CompareToDecimal(
        PeterO.Numbers.EDecimal other);

Compares an arbitrary-precision decimal number with this instance.

<b>Parameters:</b>

 * <i>other</i>: An arbitrary-precision decimal number.

<b>Return Value:</b>

Zero if the values are equal; a negative number if this instance is less, or a positive number if this instance is greater.

### CopySign

    public PeterO.Numbers.ERational CopySign(
        PeterO.Numbers.ERational other);

Returns a number with the same value as this one, but copying the sign (positive or negative) of another number.

<b>Parameters:</b>

 * <i>other</i>: A number whose sign will be copied.

<b>Return Value:</b>

An arbitrary-precision rational number.

<b>Exceptions:</b>

 * System.ArgumentNullException:
The parameter  <i>other</i>
 is null.

### Create

    public static PeterO.Numbers.ERational Create(
        int numeratorSmall,
        int denominatorSmall);

Creates a rational number with the given numerator and denominator.

<b>Parameters:</b>

 * <i>numeratorSmall</i>: A 32-bit signed integer.

 * <i>denominatorSmall</i>: A 32-bit signed integer. (2).

<b>Return Value:</b>

An arbitrary-precision rational number.

### Create

    public static PeterO.Numbers.ERational Create(
        PeterO.Numbers.EInteger numerator,
        PeterO.Numbers.EInteger denominator);

Creates a rational number with the given numerator and denominator.

<b>Parameters:</b>

 * <i>numerator</i>: An arbitrary-precision integer.

 * <i>denominator</i>: Another arbitrary-precision integer.

<b>Return Value:</b>

An arbitrary-precision rational number.

### CreateNaN

    public static PeterO.Numbers.ERational CreateNaN(
        PeterO.Numbers.EInteger diag);

Creates a not-a-number arbitrary-precision rational number.

<b>Parameters:</b>

 * <i>diag</i>: A number to use as diagnostic information associated with this object. If none is needed, should be zero.

<b>Return Value:</b>

An arbitrary-precision rational number.

<b>Exceptions:</b>

 * System.ArgumentNullException:
The parameter <i>diag</i>
 is null.

 * System.ArgumentException:
The parameter <i>diag</i>
 is less than 0.

### CreateNaN

    public static PeterO.Numbers.ERational CreateNaN(
        PeterO.Numbers.EInteger diag,
        bool signaling,
        bool negative);

Creates a not-a-number arbitrary-precision rational number.

<b>Parameters:</b>

 * <i>diag</i>: A number to use as diagnostic information associated with this object. If none is needed, should be zero.

 * <i>signaling</i>: Whether the return value will be signaling (true) or quiet (false).

 * <i>negative</i>: Whether the return value is negative.

<b>Return Value:</b>

An arbitrary-precision rational number.

<b>Exceptions:</b>

 * System.ArgumentNullException:
The parameter <i>diag</i>
 is null.

 * System.ArgumentException:
The parameter <i>diag</i>
 is less than 0.

### Divide

    public PeterO.Numbers.ERational Divide(
        PeterO.Numbers.ERational otherValue);

Divides this instance by the value of an arbitrary-precision rational number object.

<b>Parameters:</b>

 * <i>otherValue</i>: An arbitrary-precision rational number.

<b>Return Value:</b>

The quotient of the two objects.

<b>Exceptions:</b>

 * System.ArgumentNullException:
The parameter <i>otherValue</i>
 is null.

### Equals

    public override bool Equals(
        object obj);

Determines whether this object and another object are equal.

<b>Parameters:</b>

 * <i>obj</i>: An arbitrary object.

<b>Return Value:</b>

True if the objects are equal; otherwise, false.

### Equals

    public sealed bool Equals(
        PeterO.Numbers.ERational other);

Not documented yet.

<b>Parameters:</b>

 * <i>other</i>: The parameter  <i>other</i>
 is not documented yet.

<b>Return Value:</b>

A Boolean object.

### FromDouble

    public static PeterO.Numbers.ERational FromDouble(
        double flt);

Converts a 64-bit floating-point number to a rational number. This method computes the exact value of the floating point number, not an approximation, as is often the case by converting the number to a string.

<b>Parameters:</b>

 * <i>flt</i>: A 64-bit floating-point number.

<b>Return Value:</b>

A rational number with the same value as  <i>flt</i>
.

### FromEDecimal

    public static PeterO.Numbers.ERational FromEDecimal(
        PeterO.Numbers.EDecimal ef);

Converts an arbitrary-precision decimal number to a rational number.

<b>Parameters:</b>

 * <i>ef</i>: An arbitrary-precision decimal number.

<b>Return Value:</b>

An arbitrary-precision rational number.

<b>Exceptions:</b>

 * System.ArgumentNullException:
The parameter <i>ef</i>
 is null.

### FromEFloat

    public static PeterO.Numbers.ERational FromEFloat(
        PeterO.Numbers.EFloat ef);

Not documented yet.

<b>Parameters:</b>

 * <i>ef</i>: An arbitrary-precision binary float.

<b>Return Value:</b>

An arbitrary-precision rational number.

<b>Exceptions:</b>

 * System.ArgumentNullException:
The parameter <i>ef</i>
 is null.

### FromEInteger

    public static PeterO.Numbers.ERational FromEInteger(
        PeterO.Numbers.EInteger bigint);

Converts an arbitrary-precision integer to a rational number.

<b>Parameters:</b>

 * <i>bigint</i>: An arbitrary-precision integer.

<b>Return Value:</b>

The exact value of the integer as a rational number.

### FromExtendedDecimal

    public static PeterO.Numbers.ERational FromExtendedDecimal(
        PeterO.Numbers.EDecimal ef);

<b>Deprecated.</b> Renamed to FromEDecimal.

Converts an arbitrary-precision decimal number to a rational number.

<b>Parameters:</b>

 * <i>ef</i>: An arbitrary-precision decimal number.

<b>Return Value:</b>

An arbitrary-precision rational number.

<b>Exceptions:</b>

 * System.ArgumentNullException:
The parameter <i>ef</i>
 is null.

### FromExtendedFloat

    public static PeterO.Numbers.ERational FromExtendedFloat(
        PeterO.Numbers.EFloat ef);

<b>Deprecated.</b> Renamed to FromEFloat.

Not documented yet.

<b>Parameters:</b>

 * <i>ef</i>: An arbitrary-precision binary float.

<b>Return Value:</b>

An arbitrary-precision rational number.

<b>Exceptions:</b>

 * System.ArgumentNullException:
The parameter <i>ef</i>
 is null.

### FromInt32

    public static PeterO.Numbers.ERational FromInt32(
        int smallint);

Not documented yet.

<b>Parameters:</b>

 * <i>smallint</i>: The parameter  <i>smallint</i>
 is not documented yet.

<b>Return Value:</b>

An arbitrary-precision rational number.

### FromInt64

    public static PeterO.Numbers.ERational FromInt64(
        long longInt);

Not documented yet.

<b>Parameters:</b>

 * <i>longInt</i>: The parameter  <i>longInt</i>
 is not documented yet.

<b>Return Value:</b>

An arbitrary-precision rational number.

### FromSingle

    public static PeterO.Numbers.ERational FromSingle(
        float flt);

Converts a 32-bit floating-point number to a rational number. This method computes the exact value of the floating point number, not an approximation, as is often the case by converting the number to a string.

<b>Parameters:</b>

 * <i>flt</i>: A 32-bit floating-point number.

<b>Return Value:</b>

A rational number with the same value as  <i>flt</i>
.

### GetHashCode

    public override int GetHashCode();

Returns the hash code for this instance.

<b>Return Value:</b>

A 32-bit hash code.

### IsInfinity

    public bool IsInfinity();

Gets a value indicating whether this object's value is infinity.

<b>Return Value:</b>

True if this object's value is infinity; otherwise, false.

### IsNaN

    public bool IsNaN();

Returns whether this object is a not-a-number value.

<b>Return Value:</b>

True if this object is a not-a-number value; otherwise, false.

### IsNegativeInfinity

    public bool IsNegativeInfinity();

Returns whether this object is negative infinity.

<b>Return Value:</b>

True if this object is negative infinity; otherwise, false.

### IsPositiveInfinity

    public bool IsPositiveInfinity();

Returns whether this object is positive infinity.

<b>Return Value:</b>

True if this object is positive infinity; otherwise, false.

### IsQuietNaN

    public bool IsQuietNaN();

Returns whether this object is a quiet not-a-number value.

<b>Return Value:</b>

True if this object is a quiet not-a-number value; otherwise, false.

### IsSignalingNaN

    public bool IsSignalingNaN();

Returns whether this object is a signaling not-a-number value (which causes an error if the value is passed to any arithmetic operation in this class).

<b>Return Value:</b>

True if this object is a signaling not-a-number value (which causes an error if the value is passed to any arithmetic operation in this class); otherwise, false.

### Multiply

    public PeterO.Numbers.ERational Multiply(
        PeterO.Numbers.ERational otherValue);

Multiplies this instance by the value of an arbitrary-precision rational number.

<b>Parameters:</b>

 * <i>otherValue</i>: An arbitrary-precision rational number.

<b>Return Value:</b>

The product of the two numbers.

<b>Exceptions:</b>

 * System.ArgumentNullException:
The parameter <i>otherValue</i>
 is null.

### Negate

    public PeterO.Numbers.ERational Negate();

Returns a rational number with the sign reversed.

<b>Return Value:</b>

An arbitrary-precision rational number.

### Remainder

    public PeterO.Numbers.ERational Remainder(
        PeterO.Numbers.ERational otherValue);

Finds the remainder that results when this instance is divided by the value of an arbitrary-precision rational number.

<b>Parameters:</b>

 * <i>otherValue</i>: An arbitrary-precision rational number.

<b>Return Value:</b>

The remainder of the two objects.

<b>Exceptions:</b>

 * System.ArgumentNullException:
The parameter <i>otherValue</i>
 is null.

### Subtract

    public PeterO.Numbers.ERational Subtract(
        PeterO.Numbers.ERational otherValue);

Subtracts an arbitrary-precision rational number from this instance.

<b>Parameters:</b>

 * <i>otherValue</i>: An arbitrary-precision rational number.

<b>Return Value:</b>

The difference of the two objects.

<b>Exceptions:</b>

 * System.ArgumentNullException:
The parameter <i>otherValue</i>
 is null.

### ToDouble

    public double ToDouble();

Converts this value to a 64-bit floating-point number. The half-even rounding mode is used.

<b>Return Value:</b>

The closest 64-bit floating-point number to this value. The return value can be positive infinity or negative infinity if this value exceeds the range of a 64-bit floating point number.

### ToEDecimal

    public PeterO.Numbers.EDecimal ToEDecimal(
        PeterO.Numbers.EContext ctx);

Converts this rational number to a decimal number and rounds the result to the given precision.

<b>Parameters:</b>

 * <i>ctx</i>: An EContext object.

<b>Return Value:</b>

An arbitrary-precision decimal.

### ToEDecimal

    public PeterO.Numbers.EDecimal ToEDecimal();

Converts this rational number to a decimal number.

<b>Return Value:</b>

The exact value of the rational number, or not-a-number (NaN) if the result can't be exact because it has a nonterminating decimal expansion.

### ToEDecimalExactIfPossible

    public PeterO.Numbers.EDecimal ToEDecimalExactIfPossible(
        PeterO.Numbers.EContext ctx);

Converts this rational number to a decimal number, but if the result would have a nonterminating decimal expansion, rounds that result to the given precision.

<b>Parameters:</b>

 * <i>ctx</i>: An arithmetic context object to control the precision, rounding, and exponent range of the result. This context will be used only if the exact result would have a nonterminating decimal expansion. If  `HasFlags`  of the context is true, will also store the flags resulting from the operation (the flags are in addition to the pre-existing flags). Can be null, in which case this method is the same as ToExtendedDecimal.

<b>Return Value:</b>

An arbitrary-precision decimal.

### ToEFloat

    public PeterO.Numbers.EFloat ToEFloat(
        PeterO.Numbers.EContext ctx);

Converts this rational number to a binary number and rounds the result to the given precision.

<b>Parameters:</b>

 * <i>ctx</i>: An arithmetic context object to control the precision, rounding, and exponent range of the result. This context will be used only if the exact result would have a nonterminating binary expansion. If  `HasFlags`  of the context is true, will also store the flags resulting from the operation (the flags are in addition to the pre-existing flags). Can be null, in which case this method is the same as ToExtendedFloat.

<b>Return Value:</b>

An arbitrary-precision binary float.

### ToEFloat

    public PeterO.Numbers.EFloat ToEFloat();

Converts this rational number to a binary number.

<b>Return Value:</b>

The exact value of the rational number, or not-a-number (NaN) if the result can't be exact because it has a nonterminating binary expansion.

### ToEFloatExactIfPossible

    public PeterO.Numbers.EFloat ToEFloatExactIfPossible(
        PeterO.Numbers.EContext ctx);

Converts this rational number to a binary number, but if the result would have a nonterminating binary expansion, rounds that result to the given precision.

<b>Parameters:</b>

 * <i>ctx</i>: An arithmetic context object to control the precision, rounding, and exponent range of the result. This context will be used only if the exact result would have a nonterminating binary expansion. If  `HasFlags`  of the context is true, will also store the flags resulting from the operation (the flags are in addition to the pre-existing flags). Can be null, in which case this method is the same as ToExtendedFloat.

<b>Return Value:</b>

An arbitrary-precision binary float.

### ToEInteger

    public PeterO.Numbers.EInteger ToEInteger();

Converts this value to an arbitrary-precision integer. Any fractional part in this value will be discarded when converting to an arbitrary-precision integer.

<b>Return Value:</b>

An arbitrary-precision integer.

<b>Exceptions:</b>

 * System.OverflowException:
This object's value is infinity or NaN.

### ToEIntegerExact

    public PeterO.Numbers.EInteger ToEIntegerExact();

Converts this value to an arbitrary-precision integer, checking whether the value is an exact integer.

<b>Return Value:</b>

An arbitrary-precision integer.

<b>Exceptions:</b>

 * System.OverflowException:
This object's value is infinity or NaN.

 * System.ArithmeticException:
This object's value is not an exact integer.

### ToExtendedDecimal

    public PeterO.Numbers.EDecimal ToExtendedDecimal(
        PeterO.Numbers.EContext ctx);

<b>Deprecated.</b> Renamed to ToEDecimal.

Converts this rational number to a decimal number and rounds the result to the given precision.

<b>Parameters:</b>

 * <i>ctx</i>: An EContext object.

<b>Return Value:</b>

An arbitrary-precision decimal.

### ToExtendedDecimal

    public PeterO.Numbers.EDecimal ToExtendedDecimal();

<b>Deprecated.</b> Renamed to ToEDecimal.

Converts this rational number to a decimal number.

<b>Return Value:</b>

The exact value of the rational number, or not-a-number (NaN) if the result can't be exact because it has a nonterminating decimal expansion.

### ToExtendedDecimalExactIfPossible

    public PeterO.Numbers.EDecimal ToExtendedDecimalExactIfPossible(
        PeterO.Numbers.EContext ctx);

<b>Deprecated.</b> Renamed to ToEDecimalExactIfPossible.

Converts this rational number to a decimal number, but if the result would have a nonterminating decimal expansion, rounds that result to the given precision.

<b>Parameters:</b>

 * <i>ctx</i>: An arithmetic context object to control the precision. The rounding and exponent range settings of this context are ignored. This context will be used only if the exact result would have a nonterminating decimal expansion. If  `HasFlags`  of the context is true, will also store the flags resulting from the operation (the flags are in addition to the pre-existing flags). Can be null, in which case this method is the same as ToExtendedDecimal.

<b>Return Value:</b>

An arbitrary-precision decimal.

### ToExtendedFloat

    public PeterO.Numbers.EFloat ToExtendedFloat(
        PeterO.Numbers.EContext ctx);

<b>Deprecated.</b> Renamed to ToEFloat.

Converts this rational number to a binary number and rounds the result to the given precision.

<b>Parameters:</b>

 * <i>ctx</i>: An EContext object.

<b>Return Value:</b>

An arbitrary-precision binary float.

### ToExtendedFloat

    public PeterO.Numbers.EFloat ToExtendedFloat();

<b>Deprecated.</b> Renamed to ToEFloat.

Converts this rational number to a binary number.

<b>Return Value:</b>

The exact value of the rational number, or not-a-number (NaN) if the result can't be exact because it has a nonterminating binary expansion.

### ToExtendedFloatExactIfPossible

    public PeterO.Numbers.EFloat ToExtendedFloatExactIfPossible(
        PeterO.Numbers.EContext ctx);

<b>Deprecated.</b> Renamed to ToEFloatExactIfPossible.

Converts this rational number to a binary number, but if the result would have a nonterminating binary expansion, rounds that result to the given precision.

<b>Parameters:</b>

 * <i>ctx</i>: An arithmetic context object to control the precision. The rounding and exponent range settings of this context are ignored. This context will be used only if the exact result would have a nonterminating binary expansion. If  `HasFlags`  of the context is true, will also store the flags resulting from the operation (the flags are in addition to the pre-existing flags). Can be null, in which case this method is the same as ToExtendedFloat.

<b>Return Value:</b>

An arbitrary-precision binary float.

### ToSingle

    public float ToSingle();

Converts this value to a 32-bit floating-point number. The half-even rounding mode is used.

<b>Return Value:</b>

The closest 32-bit floating-point number to this value. The return value can be positive infinity or negative infinity if this value exceeds the range of a 32-bit floating point number.

### ToString

    public override string ToString();

Converts this object to a text string.

<b>Return Value:</b>

A string representation of this object. The result can be Infinity, NaN, or sNaN (with a minus sign before it for negative values), or a number of the following form: [-]numerator/denominator.

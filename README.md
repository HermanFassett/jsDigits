# jsDigits
Adds objects of type Hex, Binary, and Octal, and gives easy conversion between all three and Decimal base.

### Examples

```
var a = new Binary(1000).toDecimal().toString();
console.log(a); // 8
```

```
var a = new Hex("A7H");
a = a.add(new Hex([10, 0])); // new Hex has value A0H
console.log(a.toDecimal()); // 327
```
```
var a = new Hex(100);
var b = a.toBinary();
console.log(b.toString()); // 000100000000B
```

```
var a = new Hex(10);
var b = new Binary(10);
var c = new Octal(10);
var d = Number(10);
a = new Hex((a.toDecimal() + b.toDecimal() + c.toDecimal() + d).toHex());
console.log(a.toString()); // 24H
```

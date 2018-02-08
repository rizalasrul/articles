# Working With Object in JavaScript
Based on experience when I start learning JavaScript, understanding Object is a fundamental thing. JavaScript’s core data type is the Object data type. If you had been studying Java or .NET, you might familiar with integer, float, char, and string as primitive data type. In JavaScript — not only has primitive data type — it has complex data type, Object data type as a reference data type.

## An Object? What is it?
An object is an unordered list of primitive data type (sometimes reference data type) that is stored as a series of name-value pairs. Each item (which is known as variable) is called property, and function is called method.
This is the simple object:
```javascript
var contohObyek = {
	namaDepan : "Rizal",
	namaBelakang : "Asrul Pambudi"
};
```
We already know object is stored as a series of name-value pairs. Consider the example above, the property name are `namaDepan` and `namaBelakang`. And the value are `Rizal` and `Asrul Pambudi`.
The property names can be a string or number, but if the property name is a number, then it has to be accessed in different way. This is the example:
```javascript
var contohObyek2 = {
    nama : "Rizal Asrul Pambudi",
    93 : "My weight",
};
console.log(contohObyek2.93) // This will throw an error
console.log(contohObyek2["93"]) // Correct. This will display "My weight"
```

## Reference and primitive data type
In my opinion, one of the main differences between reference and primitive data type is the value of reference data type is stored as a reference. It’s not stored on the variable as a value. What is that mean?
```javascript
// Primitive data type number is stored as value
var umur = 24;
var umur2 = umur; // umur's value stored in umur2
umur = 20; // umur's value changed
console.log(umur) 	// 20
console.log(umur2) // 24
```
Let’s compare with the save-as-reference for objects.
```javascript
// Reference data type is stored as reference
var aLaptop = {merk : "Toshiba"};
var aLaptopBaru	= aLaptop;
aLaptop.merk = "HP";
console.log(aLaptopBaru.merk); // HP
console.log(aLaptop.merk); // HP
```
Look, the result is different, right. It’s because the value in `aLaptop` was stored as a reference and not actual value. And then when we changed the `aLaptop`’s property to “HP”, the `aLaptopBaru` reflected the change.

## Two common ways to create objects
The most common and the easiest way to create objects is with the object literal.
```javascript
// This is an empty object initialized using object literal notation
var aObjectKosong = {};
// This is an object with 4 items using object literal notation too
var aPisang	= {
  warna : "kuning",
  bentuk : "panjang",
  harga	: 5000,
  tentangRasa : function() { // This is the example of create method in object
    console.log("sangat enak");
  },
};
```
The second way is with object constructor. A constructor is a function used for initializing new object, and we use new keyword to call it.
```javascript
// This is an empty object initialized using object constructor notation
var aPisang	= new Object();
// And then we initialize it with 4 items
aPisang.warna = "kuning";
aPisang.bentuk = "panjang";
aPisang.harga = 5000;
aPisang.tentangRasa = function() {
  console.log("sangat enak");
};
```

## Conclusion
JavaScript’s core — most often used and most fundamental — data type is the Object data type. One of the main differences between reference data type (such as object) and primitive data types is reference data type’s value is stored as a reference, it is not stored directly on the variable, as a value, as the primitive data types are. These are the two common ways to create objects: object literal and object constructor.

In the next post, I will write about when the best way to use object literal or object constructor.

Wrote with love by [Rizal Asrul Pambudi][df1].

[df1]: <https://medium.com/@rizalasrul/>

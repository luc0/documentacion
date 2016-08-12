# ECMA 6

Scope vars / functions
```
{
  // scope
}
```

####Arrow functions 
REF
_( {arg1, arg2} ) => ( {return 1, return 2} )_
_( arg1 ) => ( return 1 )_
```
odds  = evens.map(v => v + 1)
pairs = evens.map(v => ({ even: v, odd: v + 1 }))
nums  = evens.map((v, i) => v + i)
this.nums.forEach((v) => {
    if (v % 5 === 0)
        this.fives.push(v)
})
```

####Funciones. Valor por default de var.
```
function f (x, y = 7, z = 42) {
    return x + y + z
}
```


####Parametros restantes
```
// Parametros restantes
function f (x, y, ...a) {
    return (x + y) * a.length
}

// Volcar parametros
var params = [ "hello", true, 7 ]
var other = [ 1, 2, ...params ] // [ 1, 2, "hello", true, 7 ]
```

####Concatenar
```
var message = `Hello ${customer.name},
want to buy ${card.amount} ${card.product} for
a total of ${card.amount * card.unitprice} bucks?`
```


####Asignar propiedades (cuando coinciden keys)
```
// asignar props, cuando coincidan keys.
obj = { x, y } // igual a obj = { x: x, y: y };

// asigna a las vars, propiedades del objeto.
var { op, lhs, rhs } = getASTNode()
```


####Objeto. Definir funciones.
```
obj = {
    foo (a, b) {
        …
    },
    bar (x, y) {
        …
    }
}
```


####Objeto.Asignar propiedades dentro de otro objeto.
```Object.assign(dst, src1, src2)```

####Array. Find element.
```
// condiciones
[ 1, 3, 4, 2 ].find(x => x > 3) // 4

// aparicion
"hello".startsWith("ello", 1) // true
"hello".endsWith("hell", 4)   // true
"hello".includes("ell")       // true
"hello".includes("ell", 1)    // true
"hello".includes("ell", 2)    // false
```

####Type check
```
Number.isNaN(42) === false
Number.isFinite(123) === true
```
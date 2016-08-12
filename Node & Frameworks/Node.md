# NODE 


## foreach con `next`
using async:
```
async.each(array, function(game, nextIteration) {
  ...
}, function(err) {
  ...
});
```
_( sirve para cuando es necesario esperar una promise dentro del each )_
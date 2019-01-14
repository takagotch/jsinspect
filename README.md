### jsinspect
---
https://github.com/danielstjules/jsinspect

```
npm install -g jsinsepct
jsinspect -t 50 --ignore "test" ./path/to/src
```

```yml
before_script:
  - "npm install -g jsinspect"
script:
  - "jsinspect ./path/to/src"
  
script:
  - "jsinspect ./path/to/src || true"
```

```
<?xml version="1.0" encoding="utf-8"?>
<pmd-cpd>
<duplication lines="10" id="xxxxxxxxxxx">
<file path="/jsinspect/spec/fixtures/intersection.js" line="1"/>
<file path="/jsinspect/spec/fixtures/intersection.js" line="1"/>
<codefragment>
spec/fixtures/intersection.js:1,5
function intersectionA(array1, array2){
  array1.filter(function(n){
    return array2.indexOf(n) != -1;
  });
}
spec/fixtures/intersection.js:7,11
function intersectionB(arrayA, arrayB){
  arrayA.filter(function(n){
    return arrayB.indexOf(n) != -1;
  });
}
</codefragment>
</duplication>
</pmd-cpd>
```



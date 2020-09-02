---
title: javascript中false的几种情况
date: 2020-07-15 20:18:59
tags: javascript
categories: javascript
---


1. false
2. undefined
3. null
4. 0 或 0.0
5. ‘’ 或 “”
6. NaN

### 利用！取反运算符
```
!!undefined // true

!null // true

!0 // true

!NaN // true

!"" // true

!54 // false

!'hello' // false

![] // false

!{} // false
```

### []和{} 为true

```
if([]){
    console.log('[] is true')
}

// [] is true


 if({}){
    console.log('{} is true')
}

// {} is true
```
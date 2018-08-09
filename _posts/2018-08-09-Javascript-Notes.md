---
layout: post
title: "Javascript Notes"
description: "Javascript Notes"
date: 2018-08-09 17:20:00+0800
categories: [javascript]
tags:
  - javascript
author: kisaku
image:
comments: true
---

##### Index: 
*   [Dump function script](#dump-function-script)
*   [How to use Call, Apply, Bind](#how-to-use-call-apply-bind)
*   [Promise](#promise) 


##### Dump function script
dump.js:  
{: .text-info}
```vim
function func1(){
  console.log("func1!!");
}
console.log(func1.toString());
```
<div markdown="1">
If you know nodejs, you can use `node` to do test as below.  
</div>
{: .well}
```
node dump.js
```
---
##### How to use Call, Apply, Bind  
<br/>
<p markdown="1">Call and apply are the other ways to call function. The first parameter will replace `this`, and the difference between `call` and `apply` is the rest parameters. Call uses normal parameter input, and apply uses the array-based parameter input.</p>
<p>Normal function call: </p>
Example:  
{: .text-info}
```vim
var obj={
  x:5,
  z:'zzz',
  func1:function(){
    console.log('this.x: '+this.x+', this.y: '+this.y+', this.z: '+this.z+', arguments: '+JSON.stringify(arguments));
  }
}
obj.func1();
```
Output:  
{: .text-danger}
<div markdown="1"  class="d-block bg-output"> 
```
this.x: 5, this.y: undefined, this.z: zzz, arguments: {}
```
</div>
<p>Use `call` to call function:  </p>
Example:  
{: .text-info}
```vim
var obj={
  x:5,
  z:'zzz',
  func1:function(){
    console.log('this.x: '+this.x+', this.y: '+this.y+', this.z: '+this.z+', arguments: '+JSON.stringify(arguments));
  }
}
obj.func1.call({x:10,y:5}, "argv1", "argv2");
```
Output:  
{: .text-danger}
<div markdown="1"  class="d-block bg-output"> 
```
this.x: 10, this.y: 5, this.z: undefined, arguments: {"0":"argv1","1":"argv2"}
```
</div>
<p>Use `apply` to call function:  </p>
Example:  
{: .text-info}
```vim
var obj={
  x:5,
  z:'zzz',
  func1:function(){
    console.log('this.x: '+this.x+', this.y: '+this.y+', this.z: '+this.z+', arguments: '+JSON.stringify(arguments));
  }
}
var args=[];
args.push("argv1");
args.push("argv2");
obj.func1.apply({x:10,y:5}, args);
```
Output:  
{: .text-danger}
<div markdown="1"  class="d-block bg-output"> 
```
this.x: 10, this.y: 5, this.z: undefined, arguments: {"0":"argv1","1":"argv2"}

```
</div>
---
##### Promise
To be continued...

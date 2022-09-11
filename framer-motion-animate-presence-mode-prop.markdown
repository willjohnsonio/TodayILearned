The AnimatePresence component animates elements when they are removed from the React tree. It's also used for page transistions. 

## Mode Prop

`mode` is a boolean that decides how `AnimatePresence` handles entering and existing children

* `sync` - which is the default. Makes children animate in or out as soon they are added or removed
* `wait` - The entering child will wait until the existing child has animted out
    * This replaces the deprecated `exitBeforeEnter` prop 
* `popLayout` - Exiting children will be "popped" out of the page layout, allowing elements to move in thier new layout 

```js
<AnimatePresence mode={"popLayout"}>
     
</AnimatePresence>
```

The `mode` requires React 18 and is tied into Reacts render cycle. So it works with layout animations. It also explicitly sets position so it works within flex containers, and size so it doesn’t change shape when setting position absolute.

 

# BASIC Vue Cheat Sheet

## Expressions
```html
<div id="app">
  <p> I have a {{ product }} </p>
  <p>{{ isWorking ? 'YES' : 'NO' }}</p>
  <p>{{ product.getSalePrice() }}</p>
</div>
```

## Directives
Conditional
```html
<p v-if="inStock">{{ product }}</p>
<p v-else-if="onSale">...</p>
<p v-else>...</p>
```
Show
```html
<p v-show="showProductDetails">...</p>
```
Two-way Data Binding
Only on input fields
```html
<input v-model="firstName">

v-model.lazy="..." // Sync inpus after change event
v-model.number="..." // Always returns a number
v-model.trim="..." // Strips whitespace
```
## List Rendering
```html
<li v-for="item in items" :key="item.id">
  {{ item }}
</li>
```
Using index to get position in an array
```html
<li v-for="(item, index) in items">...</li>
```
Iterate through objects
```html
<li v-for="(value, key) in object">...</li>
```
v-for inside a component
```html
<cart-product v-for="item in products" :product="item" :key="item.id">...</cart-product>
```


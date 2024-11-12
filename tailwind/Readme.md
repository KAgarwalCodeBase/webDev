# [Tailwind CSS](https://tailwindcss.com/)

## [Text color](https://tailwindcss.com/docs/customizing-colors)

Use the text-* utilities to control the text color of an element.  

Example: `<p class="text-blue-600">The quick brown fox...</p>`

Values are from [50, 100, 200, 300, 400, 500, 600, 700, 800, 900, 950]

### Hover, focus, and other states

Example: `<p class="text-slate-500 hover:text-blue-600">The quick brown fox...</p>`

### Breakpoints and media queries

```
<p class="text-blue-600 md:text-green-600">
  <!-- ... -->
</p>
```

### Arbitrary values

```
<p class="text-[#50d71e]">
  <!-- ... -->
</p>

<div class="bg-[#c0c0c0] h-10">Hello</div>
<div class="text-[#ff0cd0] h-10">Hello</div>
<div class="border border-[#ccc000] h-10">Hello</div>
```



### [Background Colors](https://tailwindcss.com/docs/background-color)
    <p class="text-white bg-red-600">Tailwind</p>
    <p class="text-white bg-blue-400">Tailwind</p>
    <p class="text-white bg-rose-700">Tailwind</p>
    <p class="text-white bg-zinc-500">Tailwind</p>
    <p class="text-white bg-amber-300">Tailwind</p>
    <p class="text-white bg-pink-700">Tailwind</p>


### [Text Decoration](https://tailwindcss.com/docs/text-decoration )

`overline`  
`underline`  
`no-underline`  
`none`  
`line-through`

example:
```
<p class="line-through">Tailwind</p>
<p class="underline">Tailwind</p>
<p class="overline">Tailwind</p>
<p class="underline decoration-blue-400">Tailwind</p>
<p class="text-purple-600 underline decoration-purple-600 bg-purple-200">Tailwind</p>

```

### [Accent Colors](https://tailwindcss.com/docs/accent-color)

    <h1>4. Accent Color</h1>
    <input type="checkbox" class="accent-indigo-500" checked>
    <input type="checkbox" class="accent-yello-600" checked>
    <input type="checkbox" class="accent-pink-700" checked>
  
## Container Spacing

### Margin
```
<h3 class="uppercase">1. Margin</h3>
<div class="m-4 bg-yellow-100">Margin all around</div>
<div class="mx-4 bg-yellow-200">Margin from x axies</div>
<div class="my-4 bg-yellow-300">Margin Y axies</div>
<div class="mt-6 bg-yellow-400">Margin Top</div>
<div class="mr-4 bg-yellow-500">Margin Right</div>
<div class="ml-2 bg-yellow-700">Margin Left</div>
<div class="mb-8 bg-yellow-600">Margin Bottom</div>

``` 

### Arbitrary Spacing
```
<div class="m-[200px] bg-slate-700">2. Margin all around</div>

```

### Padding
```
<h3 class="my-4">3. Padding</h3>
<div class="p-4 bg-lime-100">Padding all around</div>
<div class="px-4 bg-lime-200">Padding X axies</div>
<div class="py-4 bg-lime-300">Padding Y axies</div>
<div class="pt-6 bg-lime-400">Padding Top</div>
<div class="pr-4 bg-lime-500">Padding Right</div>
<div class="pb-8 bg-lime-600">Padding Bottom</div>
<div class="pl-2 bg-lime-700">Padding Left</div>

```

### Space Between X
```
<h3 class="my-4">Space Between X</h3>
<div class="flex space-x-4">
  <div class="p-3 bg-teal-100">01</div>
  <div class="p-3 bg-teal-200">02</div>
  <div class="p-3 bg-teal-300">03</div>
</div>

```

### Space Between Y

```
<h3 class="my-4">Space Between Y</h3>
<div class="flex flex-col space-y-4">
<div class="p-3 bg-teal-400">01</div>
<div class="p-3 bg-teal-500">02</div>
<div class="p-3 bg-teal-600">03</div>
```
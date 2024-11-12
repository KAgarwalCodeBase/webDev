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

## Typography

### Font Size
```
<h1>1. Font Sizes</h1>
<div class="container bg-teal-100 p-7 mb-10">
  <p class="text-xs">Tailwind is awesome</p>
  <p class="text-sm">Tailwind is awesome</p>
  <p class="text-base">Tailwind is awesome</p>
  <p class="text-lg">Tailwind is awesome</p>
  <p class="text-xl">Tailwind is awesome</p>
  <p class="text-2xl">Tailwind is awesome</p>
  <p class="text-3xl">Tailwind is awesome</p>
  <p class="text-4xl">Tailwind is awesome</p>
  <p class="text-5xl">Tailwind is awesome</p>
  <p class="text-6xl">Tailwind is awesome</p>
  <p class="text-7xl">Tailwind is awesome</p>
  <p class="text-8xl">Tailwind is awesome</p>
  <p class="text-9xl">Tailwind is awesome</p>
</div>
```

### Font Family
```
<h1>2. Font Family</h1>
<div class="container bg-indigo-200 p-10 mb-10">
  <p class="font-sans">Tailwind is awesome</p>
  <p class="font-serif">Tailwind is awesome</p>
  <p class="font-mono">Tailwind is awesome</p>
</div>
```

### Font Weight
```
<h1>3. Font Weight</h1>
<div class="container bg-orange-300 p-10 mb-10">
  <p class="font-light">Tailwind is awesome</p>
  <p class="font-normal">Tailwind is awesome</p>
  <p class="font-medium">Tailwind is awesome</p>
  <p class="font-semibold">Tailwind is awesome</p>
  <p class="font-bold">Tailwind is awesome</p>
</div>

```

### Letter Spacing
```
<h1>4. Letter Spacing</h1>
<div class="container bg-red-400 p-10 mb-10">
  <p class="tracking-tight">Tailwind is awesome</p>
  <p class="tracking-normal">Tailwind is awesome</p>
  <p class="tracking-wide">Tailwind is awesome</p>
</div>
```

### Text Alignment
```
<h1>5. Text Alighnment</h1>
<div class="container bg-amber-400 p-10 mb-10">
  <p class="text-left">Tailwind is awesome</p>
  <p class="text-center">Tailwind is awesome</p>
  <p class="text-right">Tailwind is awesome</p>
</div>

```

### Text Decoration
```
<h1>6. Text Decoration</h1>
<div class="container bg-emerald-400 p-10 mb-10">
  <p class="underline decoration-4">Tailwind is awesome</p>
  <p class="line-through">Tailwind is awesome</p>
  <p class="overline">Tailwind is awesome</p>
  <p class="no-underline">Tailwind is awesome</p>
</div>
```

### Decoration Style
```
<h1>7. Decoration Style</h1>
<div class="container bg-cyan-400 p-10 mb-10">
  <p class="underline decoration-solid">Tailwind is awesome</p>
  <p class="underline decoration-double">Tailwind is awesome</p>
  <p class="underline decoration-dotted">Tailwind is awesome</p>
  <p class="underline decoration-dashed">Tailwind is awesome</p>
  <p class="underline decoration-wavy">Tailwind is awesome</p>
</div>
```

### Decoration offset
```
<h1>8. Decoration Offset</h1>
<div class="container bg-indigo-400 p-10 mb-10">
  <p class="underline underline-offset-1">Tailwind is awesome</p>
  <p class="underline underline-offset-2">Tailwind is awesome</p>
  <p class="underline underline-offset-4">Tailwind is awesome</p>
  <p class="underline underline-offset-8">Tailwind is awesome</p>
</div>

```
### Text Transform
```
<h1>9. Text Transform</h1>
<div class="container bg-pink-400 p-10 mb-10">
  <p class="normal-case">Tailwind is awesome</p>
  <p class="uppercase">Tailwind is awesome</p>
  <p class="lowercase">Tailwind is awesome</p>
  <p class="capitalize">Tailwind is awesome</p>
</div>
```

## Sizing

### Width
```
<h1>Width All Around</h1>
<div class="bg-teal-100 p-5">
<div class="bg-teal-600 w-0">0</div>
<div class="bg-teal-600 w-1">1</div>
<div class="bg-teal-600 w-1.5">1.5</div>
```

### Percentage
```
<h1 class="mt-5">Percentages</h1>
<div class="bg-teal-200 mb-5 p-5">
<div class="bg-green-400 p-2 mb-4 w-1/2">1/2</div>
<div class="bg-green-400 p-2 mb-4 w-1/3">1/3</div>
<div class="bg-green-400 p-2 mb-4 w-2/3">2/3</div>
<div class="bg-green-400 p-2 mb-4 w-1/4">1/4</div>
<div class="bg-green-400 p-2 mb-4 w-2/4">2/4</div>
<div class="bg-green-400 p-2 mb-4 w-3/4">3/4</div>
<div class="bg-green-400 p-2 mb-4 w-1/5">1/5</div>
</div>

```

### Max Width
```
<h1 class="mt-5">Max Width</h1>
<div class="bg-yellow-100 p-10 mb-10 max-w-lg">
Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit voluptatum praesentium suscipit? Eius id natus veniam dolorem repudiandae vitae cumque ex cupiditate explicabo praesentium omnis, eligendi soluta provident quos facere!
</div>

```
### Width of the viewport
```
<h1 class="mt-5">VW & Width100%</h1>
<div class="bg-green-500 my-2 p-5 w-full">
(vw) screen
</div>
```

### 100% of container
```
<div class="bg-green-500 my-2 w-full">(width 100%) w-full</div>
```
### Arbitrary Width
```
<div class="bg-teal-500 text-white my-2 w-[500px]">
Arbitrary Width (500px)
</div>
```
### Height (Most of the same options as widths)
```
<h1 class="mt-5">Height All Around</h1>
<div class="flex items-end mt-20 mb-10">
<div class="bg-indigo-400 ml-5 h-24">height 24</div>
<div class="bg-indigo-400 ml-5 h-32">height 32</div>
<div class="bg-indigo-400 ml-5 h-40">height 40</div>
<div class="bg-indigo-400 ml-5 h-48">height 48</div>
<div class="bg-indigo-400 ml-5 h-64">height 64</div>
<div class="bg-indigo-400 ml-5 h-80">height 80</div>
</div>
```

### Min Height
```
<div class="p-5 h-[400px] bg-green-300 mb-5">
  <div class="min-h-full bg-teal-400">Take Full Height</div>
</div>
<!-- Max Height -->
<!-- https://tailwindcss.com/docs/max-height -->
<div class="h-[150px] bg-orange-200 mb-10">
  <div class="m-20 bg-orange-500 h-48 max-h-full">Max Height Full</div>
</div>
```

### Full screen height
```
<h1 class="mb-2">Full Screen Height</h1>
<div class="bg-pink-300 mb-4 h-screen">Hello</div>

<!-- Width Auto -->
<div class="bg-green-400 p-5 w-auto">Auto</div>
```
# [Tailwind CSS](https://tailwindcss.com/)

### [Text color](https://tailwindcss.com/docs/customizing-colors)

Use the text-* utilities to control the text color of an element.  

Example: `<p class="text-blue-600">The quick brown fox...</p>`

Values are from [50, 100, 200, 300, 400, 500, 600, 700, 800, 900, 950]

#### Hover, focus, and other states

Example: `<p class="text-slate-500 hover:text-blue-600">The quick brown fox...</p>`

#### Breakpoints and media queries

```
<p class="text-blue-600 md:text-green-600">
  <!-- ... -->
</p>
```

#### Arbitrary values

```
<p class="text-[#50d71e]">
  <!-- ... -->
</p>
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
  

### Arbitrary Colors

    <div class="bg-[#c0c0c0] h-10">Hello</div>
    <div class="text-[#ff0cd0] h-10">Hello</div>
    <div class="border border-[#ccc000] h-10">Hello</div>

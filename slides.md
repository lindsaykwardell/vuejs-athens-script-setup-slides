---
# try also 'default' to start simple
theme: purplin
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
# highlighter: shiki
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
---

<h1 class="font-mono">&lt;script setup&gt;</h1>



<div class="flex justify-center">
  <div class="w-50 h-40 p-1 mt-5 flex items-center justify-center">
  <div class="text-5xl">{</div>
  <div class="w-38 h-38 p-5">
  
  ![](https://vuejs.org/images/logo.svg)
  
  </div>
  <div class="text-5xl">}</div>
  </div>
</div>


<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

<div grid="~ cols-3 gap-2 ">

![](/lindsay.jpg)

<div class="col-span-2 text-center flex flex-col justify-between">

# Lindsay Wardell

<v-clicks>

<div>

#### Full Stack Engineer

<img src="https://www.noredink.com/assets/logo-red-black-f6989d7567cf90b349409137595e99c52d036d755b4403d25528e0fd83a3b084.svg" class="w-1/3 bg-white p-3 m-auto mt-4">

</div>

https://www.noredink.com/jobs

</v-clicks>

<div class="flex justify-around">

<v-clicks>

<img src="https://devchat.tv/wp-content/uploads/2020/06/viewsonvue-1-scaled-768x768.jpg" class="w-32" />

</v-clicks>

</div>

</div>

</div>

<div class="abs-bl m-6 text-xl !border-none text-right">
  <div class="flex">
    <carbon-logo-twitter class="w-16" />  <span>lindsaykwardell</span>
  </div>
  <div class="flex">
    <carbon-logo-github class="w-16" /> <span> lindsaykwardell</span>
  </div>
  <div class="flex underline">
    <div class="w-16" /> lindsaykwardell.com
  </div>
</div>

---

# What is &lt;script setup&gt;?

> &lt;script setup&gt; is a compile-time syntactic sugar for using Composition API inside Single File Components (SFCs). It is the recommended syntax if you are using both SFCs and Composition API.

<v-click>

```js {all|3-7|8-12|13-17|all}
<script>
export default {
  data() {
    return {
      name: ''
    }
  },
  computed: {
    isNamePresent() {
      return this.name.length > 0
    }
  },
  methods: {
    submitName() {
      console.log(this.name)
    }
  }
}
</script>
```

</v-click>

---

# What is &lt;script setup&gt;?

> &lt;script setup&gt; is a compile-time syntactic sugar for using Composition API inside Single File Components (SFCs). It is the recommended syntax if you are using both SFCs and Composition API.

```js {all|2|5|6-11|13-17|all}
<script>
import { ref, computed } from 'vue'

export default {
  setup() {
    const name = ref('')
    const isNamePresent = computed(() => name.value.length > 0)

    function submitName() {
      console.log(name.value)
    }

    return {
      name,
      isNamePresent,
      submitName
    }
  }
}
</script>
```

---

# What is &lt;script setup&gt;?

> &lt;script setup&gt; is a compile-time syntactic sugar for using Composition API inside Single File Components (SFCs). It is the recommended syntax if you are using both SFCs and Composition API.

```js {all|1|999|all}
<script setup>
import { ref, computed } from 'vue'

const name = ref('')
const isNamePresent = computed(() => name.value.length > 0)

function submitName() {
  console.log(name.value)
}
</script>
```

<v-clicks>

- Code is simpler to read
- Improved runtime performance
- Better Typescript integration (`<script setup lang="ts">`)
  - Improved IDE type performance

</v-clicks>

---
layout: center
---

# Coding Time!

---
layout: center
---

<img src="/todo-pre-coding.png" class="w-1/2 m-auto">

---
layout: center
---

<img src="/todo-post-coding.png" class="w-1/2 m-auto">

---
layout: center
---

<div class="flex justify-center">
  <div class="w-50 h-40 p-1 mt-5 flex items-center justify-center">
  <div class="text-5xl">{</div>
  <div class="w-38 h-38 p-5">
  
  ![](https://vuejs.org/images/logo.svg)
  
  </div>
  <div class="text-5xl">}</div>
  </div>
</div>

<v-clicks>

- https://v3.vuejs.org/api/sfc-script-setup.html
- https://github.com/lindsaykwardell/vuejs-athens-code-example

</v-clicks>
<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
  </div>
</template>

<script lang="ts">
import { useMousePosition } from '@/hooks/mouse'
import HelloWorld from '@/components/HelloWorld.vue' // @ is an alias to /src

export default {
  components: {
    HelloWorld,
  },
  setup() {
    const { x, y } = useMousePosition()

    console.log(x, y)
    interface IDeveloper {
      name: string
      age?: number
    }
    class def implements IDeveloper {
      name = 'xx'
      age = 10
    }
    // OK
    class dev extends def {}
    console.log(new dev())
  },
}
// @Options({
//   components: {
//     HelloWorld,
//   },
//   created() {
//     interface IDeveloper {
//       name: string
//       age?: number
//     }
//     class def implements IDeveloper {
//       name = 'xx'
//       age = 10
//     }
//     // OK
//     class dev extends def {}
//     console.log(new dev())
//   },
// })
// export default class Home extends Vue {}
</script>

### `experimentalResolveStyleCssClasses` regression reproduction

**Prerequisites:**
1. In `tsconfig`
```ts
 "vueCompilerOptions": {
    "experimentalResolveStyleCssClasses": "always",
  },
```
2. `<style>` without `scoped` (see `src/components/HelloWorld.vue` in this repo)

**Actual result**: classes have no references even when `experimentalResolveStyleCssClasses` set to `always`

**Expected result**: classes have references

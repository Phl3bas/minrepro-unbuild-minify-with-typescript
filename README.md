min repo for minify bug


```typescript

export default defineBuildConfig({
  entries: [
    'src/index',
  ],
  declaration: true, // this line as true along with rollup.esbuild.minify = true crashes
  clean: true,
  rollup: {
    emitCJS: true,
    esbuild: {
        minify: true,
        target: 'es2015',
    },
    dts: {}
  },
})


```
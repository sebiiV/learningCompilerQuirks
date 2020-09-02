# LearningCompilerQuirks
Repo for experimenting with weird behaviour

## Static Volatile vs const

### Func1 assembly
`static const volatile char a[] = { 0x13,0x37,0x13,0x37,0x13,0x37...};`

![alt_text](https://github.com/sebiiV/learningCompilerQuirks/blob/master/screenshots/func1.png?raw=true)


### Func2 assembly
`    const char b[] = { 0x66,0xFF,0xCC,0x66,0xFF,0xCC,0x66,0xFF,0xCC,0x66...};`

![alt_text](https://github.com/sebiiV/learningCompilerQuirks/blob/master/screenshots/func2.png?raw=true)


the difference is that the func2 byte array is being assembled at runtime through lots of **mov** commands so the sstring isn't present in the binary on disk (.data segment)

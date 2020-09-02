# LearningCompilerQuirks
Repo for experimenting with weird behaviour

## Static Volatile vs const

### Func1 assembly
![alt_text](https://github.com/sebiiV/learningCompilerQuirks/blob/master/screenshots/func1.png?raw=true)
### Func2 assembly
![alt_text](https://github.com/sebiiV/learningCompilerQuirks/blob/master/screenshots/func2.png?raw=true)


the difference is that the func2 byte array is being assembled at runtime through lots of **mov** commands so the sstring isn't present in the binary on disk (.data segment)

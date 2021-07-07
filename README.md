OSX | Linux | Node 4.1-14.x, Python2/3:
[![Build Status](https://travis-ci.org/homfen/ems.svg?branch=master)](https://travis-ci.org/homfen/ems)
[![npm version](https://badge.fury.io/js/ems-typed.svg)](https://www.npmjs.com/package/ems-typed)

# Extended Memory Semantics (EMS)

**EMS makes possible persistent shared memory parallelism between Node.js, Python, and C/C++**.

Extended Memory Semantics (EMS) unifies synchronization and storage primitives
to address several challenges of parallel programming:

- Allows any number or kind of processes to share objects
- Manages synchronization and object coherency
- Implements persistence to non-volatile memory and secondary storage
- Provides dynamic load-balancing between processes
- May substitute or complement other forms of parallelism

#### original package

[ems](https://www.npmjs.com/package/ems)

## updates:

add TypedArray support.

```
// node.js
const img = new Uint8Array(1920*1080*4);
shared.writeEF('img', img);

// python
img = shared.readFE('img')
print(len(img))
```

## build

```
// node.js
npm run build

// python
sudo make clean_py3
sudo make py3
```

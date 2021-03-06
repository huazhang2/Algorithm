## Algorithm
- Thoughts come from Web or classical books like 'Introduction to Algorithms, Third Edition'
- Some source will generate dynamic library, for outer usage
- Can be directly compiled on MAC and Linux
- Key kind of algorithm
    - 8+ kind of sort
        - Linear
            - bucketSort
            - radixSort
        - O(Nlog(N))
            - quickSort
            - quickSortOptimized
            - shellSort
            - heapSort
            - mergeSort
        - O(N^2)
            - bubbleSort
            - insertSort
    - kmp
        - kmp
        - kmpOptimized
    - rbtree

## Quick Start
- kmp & sort need c++11 support
- rbtree is a standalone source
```bash
make -j
source env.sh (need not for MAC)
ldd bin/sortdemo
        linux-vdso.so.1 =>  (0x00007fffe4fc2000)
        libmybasic.so => ./lib/libmybasic.so (0x00007fae138aa000)      <== mylib
        libmysort.so => ./lib/libmysort.so (0x00007fae136a0000)        <== mylib
        libstdc++.so.6 => /usr/lib/x86_64-linux-gnu/libstdc++.so.6 (0x00007fae1331e000)
        libgcc_s.so.1 => /lib/x86_64-linux-gnu/libgcc_s.so.1 (0x00007fae13108000)
        libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007fae12d3e000)
        libm.so.6 => /lib/x86_64-linux-gnu/libm.so.6 (0x00007fae12a35000)
        /lib64/ld-linux-x86-64.so.2 (0x00007fae13aad000)

binary was under ./bin
```

### Example
#### Sort
``` bash
source env.sh
```

```bash
./bin/sortdemo
||=>> Select Sort Algorithm @
[1]: Bubble Sort       [2]: Insert Sort       [3]: Quick  Sort
[4]: Quick  Sort(Op)   [5]: Shell  Sort       [6]: Heap   Sort
[7]: Merge  Sort       [8]: Bucket Sort       [9]: Radix  Sort
[10]:Library Fun       [*]: Quit Selection
-------------------------- Original Array --------------------------
49 -85 -98 -78 -44 30 -48 66 63 89 6 -58 66 83 91 76 -7 -72 88 -23
Input Here: 3
-------------------------- Quick Sort --------------------------
-98 -85 -78 -72 -58 -48 -44 -23 -7 6 30 49 63 66 66 76 83 88 89 91

||=>> Select Sort Algorithm @
[1]: Bubble Sort       [2]: Insert Sort       [3]: Quick  Sort
[4]: Quick  Sort(Op)   [5]: Shell  Sort       [6]: Heap   Sort
[7]: Merge  Sort       [8]: Bucket Sort       [9]: Radix  Sort
[10]:Library Fun       [*]: Quit Selection
-------------------------- Original Array --------------------------
11 -91 40 -37 -84 31 44 -62 -11 -67 -33 -34 60 -81 77 40 -7 82 13 17
Input Here: 5
-------------------------- Shell Sort --------------------------
-91 -84 -81 -67 -62 -37 -34 -33 -11 -7 11 13 17 31 40 40 44 60 77 82
```

#### KMP
You may know well about the next array from below two figures.

![next1](http://img1.tuicool.com/2E36nuQ.png!web)

![next2](http://img1.tuicool.com/qYN3u2v.png!web)

``` bash
source env.sh
```
```bash
./bin/kmpdemo
basic kmp:
str = BBCABCDABABCDABCDABDET
pattern = BCDABDE
-1 0 0 0 0 1 0
Index = 14

optimized kmp:
str = BBCABCDABABCDABCDABDET
pattern = BCDABDE
-1 0 0 0 1 1 0
Index = 14
```

## License
The [MIT](./LICENSE.txt) License (MIT)

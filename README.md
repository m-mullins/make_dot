# Produce graph dot diagrams of makes dependency tree
* A new "-G" option will now produce graphviz dot file compatible output of the make dependency tree.
* Filters for "*.c" and "*.o" targets

# Example 1 for main.o
```
make -G main.o 2>/dev/null  | dot -Tpng >examples/main.png
```
![main.png](https://rawgit.com/m-mullins/make_dot/master/examples/main.png)

# Example 2 for loadavg target
```
make -G loadavg 2>/dev/null  | dot -Tpng >examples/loadavg.png
```
![loadavg.png](https://rawgit.com/m-mullins/make_dot/master/examples/loadavg.png)

# Example 3 for the make binary
```
make -G make 2>/dev/null | dot -Tpng >./example/make.png
```
![make.png](https://rawgit.com/m-mullins/make_dot/master/examples/make.png)

# Example 4 in the glob/ directory
```
make -C glob -G libglob.a  2>/dev/null | dot -Tpng >./example/glob.png
```
![glob.png](https://rawgit.com/m-mullins/make_dot/master/examples/glob.png)


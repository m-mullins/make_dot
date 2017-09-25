# Produce graph dot diagrams of makes dependency tree
* A new "-G" option will now produce graphviz dot file compatible output of the make dependency tree.
* Use on small projects.

# TODO
* Need to make sure it only prints the graphs for a particular target

# Example 1 in the glob/ directory
```
make -C glob -G libglob.a | dot -Tpng >./example/glob.png
```
![glob.png](https://rawgit.com/m-mullins/make_dot/master/examples/glob.png)
# Example 2 for the make binary
```
make -G make | dot -Tpng >./example/make.png
```
![make.png](https://rawgit.com/m-mullins/make_dot/master/examples/make.png)

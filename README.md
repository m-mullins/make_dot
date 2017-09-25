# Produce graph dot diagrams of makes dependency tree
* A new "-G" option will now produce graphviz dot file compatible output of the make dependency tree.
* Was probably a huge mistake as even running it on this project the graph is very big (see below).

# Example 1 in the glob/ directory
```
make -C glob -G libglob.a | dot -Tpng >./example/glob.png
```
# Example 2 for the make binary
```
make -G make | dot -Tpng >./example/glob.png
```

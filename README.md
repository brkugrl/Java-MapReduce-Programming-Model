# Java-MapReduce-Programming-Model
MadReduce is a programming model that can be used to process and generate big datasets. While doing this, this algorithm uses 2 different methods which are mapFunc(Map function) and reduceFunc(Reduce function). In mapFunc, datas will be taken and these datas are converted into 
another set of datas. Each elements of the original data is converted into tuples(key/value pairs) after calling the mapFucn. In reduceFunc, input (the output of the mapFunc) will be taken and that input is filtered out for reducing the number of tuples(key/value pairs). reduceFunc must always be called after mapFunc, otherwise MapReduce programming model does not work properly. An example of MapReduce algorithm can be seen below.

mapFunc("berke ugurlu berke berke john coltrane", "doc1" )
mapFunc("berke kulu berke kulu", "doc2" )
Set of Datas after calling mapFunc
[berke, doc1, ugurlu, doc1, berke, doc1, berke, doc1, john, doc1, coltrane, doc1, berke, doc2, kulu, doc2, berke, doc2, kulu, doc2]
Result of the MapReduce algorithm after calling reduceFunc
[berke, [doc1, doc2], ugurlu, [doc1], john, [doc1], coltrane, [doc1], kulu, [doc2]]


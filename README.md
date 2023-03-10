## Русский:

### Пункт 1.
При построении матрицы смежности по графу необходимо обозначить количество вершин, исходя из этого построим матрицу размерностью N на N. Далее заполняем матрицу построчно. Строка — первая вершина. Столбец — вторая вершина. Если между первой и второй есть связь (дуга идёт во вторую), то ставится один, иначе — ноль. 

**Входные данные:** количество вершин, граф.

**Выходные данные:** матрица смежности.

### Пункт 2.
Построение матрицы смежности по матрице весов. Проходимся по каждому элементу матрицы весов, если же элемент не равен нулю, то ставим единицу, иначе ноль.

```Function Weights2Adj(Weights: Matrix; Size: integer): Matrix;
Var AdjMatrix: Matrix;
    i, j: integer;
Begin
  for i:=1 to Size do
    for j:=1 to Size do
      if Weights[i, j] <> 0 then
        AdjMatrix := 1
      else
        AdjMatrix := 0;

  Result := AdjMatrix;
End;```

### Пункт 3.
Построение матрицы инцидентности по матрице смежности осуществляется проходом по столбцам. Количество ребёр — количество единиц в матрице смежности. Строим матрицу N на M, где N — количество вершин, а M — количество рёбер. Строка элемента равного единице в матрице смежности — откуда идёт дуга (начало — 1), столбец элемента равного единице в матрице смежности — куда идёт дуга (конец — -1).


## English:

### Item 1.
When constructing the adjacency matrix along the graph, it is necessary to denote the number of vertices, based on this, we will build a matrix with dimension N by N. Next, fill in the matrix line by line. The row is the first vertex. The column is the second vertex. If there is a connection between the first and the second (the arc goes to the second), then one is put, otherwise zero. 

**Input data:** number of vertices, graph.
**Output:** adjacency matrix.

### Item 2.
Construction of the adjacency matrix by the matrix of weights. We go through each element of the matrix of weights, if the element is not zero, then we put one, otherwise zero.

```Function Weights2Adj(Weights: Matrix; Size: integer): Matrix;
Var AdjMatrix: Matrix;
    i, j: integer;
Begin
  for i:=1 to Size do
    for j:=1 to Size do
      if Weights[i, j] <> 0 then
        AdjMatrix := 1
      else
        AdjMatrix := 0;

  Result := AdjMatrix;
End;```

### Item 3.
The construction of the incidence matrix by the adjacency matrix is carried out by passing through the columns. The number of edges is the number of units in the adjacency matrix. We construct a matrix N by M, where N is the number of vertices and M is the number of edges. The row of an element equal to one in the adjacency matrix is where the arc comes from (beginning — 1), the column of an element equal to one in the adjacency matrix is where the arc goes (end — -1).

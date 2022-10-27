---
layout: post
title: Summary about Gurobi
date: 2022-07-16
categories: Programming
tags: [Gurobi]
description: Some skills about gurobi.
---

## addMVar vs addVar

For MVar, 

z = m.addMVar(shape = W, vtype=GRB.CONTINUOUS)

just use z[0] to indicate the first variable.

For Var,

x ={}

for i in range(1,3):
    x[i] = model.addVar(lb = 0, ub = GRB.INFINITY, vtype = GRB.CONTINUOUS, name = 'x_' + str(i))

Use x[1] to indicate the first variable.

## addConstrs() vs addConstr()

model.addConstrs(x.sum(i, '*') <= capacity[i] for i in range(5))

m.addConstrs((x[i,j] == 0 for i in range(4)
                            for j in range(4)
                            if i != j), name='c')

----------------------------------------------

m.addConstr(x <= 1, name='c0')

for i in range(2):
        m.addConstr(x[i] + z[i] <= d[i])


## Some mistakes you may make

1.
Notice that 

addMVar (shape, lb=0.0, ub=float('inf'), obj=0.0, vtype=GRB.CONTINUOUS, name="" )

The lower bound is non-negative by default.

2.
How to obtain the variables.

Bear in mind that the difference between global and local variables in the function.

----------------

m.getVarByName('varz[' + str(k) + ']')

k should be an integer.

ensure getvar is not None.

Two ways to change the type of variables

1. 
```python
v = m.getVarByName('pi[' + str(1) + ']')
v.vtype = GRB.BINARY
```

```python
for var in m.getVars():
    var.vtype = GRB.BINARY
```

Ways to change the constraints:

1.
Search model.chgCoeff(c0, x, 2.0)

2. 
vx1 = m.getVarByName('x3')

m.getConstrByName('c1')

m.getCoeff(cc1,vx1)

Note that querying by name can be slow, so either try to avoid it, or do it once (and store the result in a dictionary).

3.  
```python
for cnstr in model.getConstrs():
        print(cnstr.sense, cnstr.rhs)
```

4. 
```python 
for cnstr in pre.getConstrs():
    for var in pre.getVars():
        print(pre.getCoeff(cnstr, var), end=" ")
```

5. 
```python   
for cnstr in model.getConstrs():
    print("Constraint %s: sense %s, RHS=%f" % (cnstr.ConstrName, cnstr.Sense, cnstr.RHS))
    row = model.getRow(cnstr)
    for k in range(row.size()):
        print("Variable %s, coefficient %f" % (row.getVar(k).VarName, row.getCoeff(k))
```

c1 = model.addConstr(x + y >= 1.0, "c1")
c1.rhs = 2.0

To change all rhs. Search Model.setAttr()
model.setAttr("rhs", conss, values)

----------------------------------
> print(m.display()) 

It will print out the model.


----------------------------------
Several ways to change model.

1. If you want to adjust a model from the existing model, you can only get the var and constrs by name.

2. You could write the adjustment in one function, then change the existing model.

3. Use import from another file, you can also use the defined variables.
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
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


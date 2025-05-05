import math
def g(x):
    return math.cos(x)
def simple_iteration_method(a, b, epsilon=1e-6, max_iter=100):
    x0 = (a + b) / 2.0 
    iter_count = 0
    while iter_count < max_iter:
        x1 = g(x0)
        if abs(x1 - x0) < epsilon:
            return x1 
        x0 = x1
        iter_count += 1
    return None
a = 0.0
b = 1.0
root = simple_iteration_method(a, b)
if root is not None:
    print(f"Təqribi kök: {root}")
else:
    print("Kök tapılmadı.")

import matplotlib.pyplot as plt
import numpy as np

# consider a cube of dx , dy , dz lengths and having heat transfer only in x
# dirtn and internally,uniform heat generation 

q = 120 # W --- heat generate
k = 43 # (W/m-K) --- thermal conductivity
T2 = (273 + 40) # temp at other side (cold) --- K
T1 = (273 + 44) # temp at first side (hot) --- K
L = 3 # slab length --- m
# x = 3 # arbitary point for finding temp (from hot side as refn point) --- m

a = -(q/(2*k))
b = (((T2 - T1)/L) + ((q*L)/(2*k)))
c = T1

def myfunc(x):
  # T = (-(q*(x**2))/(2*k)) + (((T2 - T1)*x)/L) + ((q*L*x)/(2*k)) + T1
  T = (a*(x**2)) + (b*x) + c
  return T

xpoints = np.array([i for i in range(0,L*100,10)]) # points in cm 

# print(xpoints)

ypoints = np.array([myfunc(j/100) for j in xpoints]) # points in K

# print(ypoints)
print(f"point with 0 temp is: {np.roots([a,b,c])} m")
stat_point = ((-b)/(2*a))
print(f"stationary point: {stat_point}\ntemp at point is: {myfunc(stat_point)-273} deg C")


for a,b in enumerate(ypoints):
  print(f"Temp at {a*10} cm is: {b-273} deg C")

print(f"Max temp is: {max(ypoints)-273} deg C")
print(f"Min temp is: {min(ypoints)-273} deg C")
plt.plot(xpoints, (ypoints-273))
plt.xlabel("postion in cm")
plt.ylabel("temp in deg C")
plt.show()

# Data-structure-partical-program-13
import time

products=[50,20,70,10,40]
key=input("Enter product ID to search: ")

# Linear Search
start=time.time()
for i in range(len(products)):
    if products[i]==key:
        print "Linear Search Found"
        break
end=time.time()
print "Linear Time:",end-start

# Binary Search
products.sort()
start=time.time()
low=0
high=len(products)-1

while low<=high:
    mid=(low+high)/2
    if products[mid]==key:
        print "Binary Search Found"
        break
    elif key<products[mid]:
        high=mid-1
    else:
        low=mid+1

end=time.time()
print "Binary Time:",end-start

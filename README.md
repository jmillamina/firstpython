# firstpython

PERSONS = [
{"NAME": "JOHN", "AGE": 12, "LOCATION": "PASIG"},
{"NAME": "DOE", "AGE": 15, "LOCATION": "PAMPANGA"},
{"NAME": "JIGS", "AGE": 5, "LOCATION": "QUEZON"},
{"NAME": "MARIE", "AGE": 30, "LOCATION": "PARANAQUE"},
{"NAME": "JOANNE", "AGE": 18, "LCATION": "PARANAQUE"},
]

#Program for filter by age range
import headq
age_min = heapq.nsmallest(1, PERSONS, key=lambda s: s["AGE"])
age_max = heapq.nlargest(1,PERSONS, key=lambda s: s["AGE"])

print(age_min) #It will print the youngest among the group
print(age_max) #It will print the oldest among the group

#Program for filter by location
from operator import itemgetter
from itertools import groupby
PERSONS.sort(key=itemgetter("LOCATION"))
for LOCATION, items in groupby(PERSONS, key =itemgetter("LOCATION")):
	print(LOCATION) #It will print the location
	for i in items:
		print(" ",i) #It will print the datas according to its location
    
#Program for sorted name
name = sorted(PERSONS, key=itemgetter("NAME"))
print(name) #It will print the datas in ascending order

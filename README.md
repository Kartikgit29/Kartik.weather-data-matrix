#python program for weather data matrix
cities = ["Delhi", "Mumbai", "Chennai", "Kolkata", "Bangalore"]
days = ["Mon", "Tue", "Wed", "Thu", "Fri"]

weather_data = [
    [32, 33, 34, 31, 30],  # Delhi
    [28, 29, 31, 32, 30],  # Mumbai
    [35, 36, 34, 33, 32],  #Chennai
    [30, 31, 29, 28, 27],  #Kolkata
    [25, 26, 27, 28, 29]  #banglore
]
print("=== Weather Data Matrix (°C) ===\n")
print(f"{'City':<12}", end="")
for d in days:
    print(f"{d:<8}", end="")
print("\n" + "-" * 52)

for i in range(len(cities)):
    print(f"{cities[i]:<12}", end="")
    for j in range(len(days)):
        print(f"{weather_data[i][j]:<8}", end="")
    print()

print("\n=== Average Temperature ===")
for i in range(len(cities)):
    avg_temp = sum(weather_data[i]) / len(days)
    print(f"{cities[i]:<12}: {avg_temp:.2f}°C")

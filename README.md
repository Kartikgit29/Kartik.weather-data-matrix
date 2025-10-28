cities = ["Delhi", "Mumbai", "Chennai", "Kolkata", "Bangalore"]
days = ["Mon", "Tue", "Wed", "Thu", "Fri"]


weather_data = [
    [32, 33, 34, 31, 30],  # Delhi
    [28, 29, 31, 32, 30],  # Mumbai
    [35, 36, 34, 33, 32],  # Chennai
    [30, 31, 29, 28, 27],  # Kolkata
    [25, 26, 27, 28, 29]   # Bangalore
]

print("🌤️  Weekly Weather Report (in °C)")
print("=" * 45)


print(f"{'City':<12}", end="")
for day in days:
    print(f"{day:<8}", end="")
print("\n" + "-" * 45)


for i, city in enumerate(cities):
    print(f"{city:<12}", end="")
    for temp in weather_data[i]:
        print(f"{temp:<8}", end="")
    print()

print("\n📊 Average Temperatures for the Week")
print("-" * 45)


for i, city in enumerate(cities):
    avg_temp = sum(weather_data[i]) / len(days)
    print(f"{city:<12}: {avg_temp:.2f}°C")

print("\n🌡️  Stay cool and hydrated this week!")

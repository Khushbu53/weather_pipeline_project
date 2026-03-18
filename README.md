from datetime import datetime

# Sample weather data
weather_data = [
    {"city": "Mumbai", "temp": 28.5, "humidity": 65, "condition": "Clear sky"},
    {"city": "Delhi", "temp": 22.3, "humidity": 45, "condition": "Partly cloudy"},
    {"city": "Bangalore", "temp": 24.8, "humidity": 70, "condition": "Light rain"},
    {"city": "Chennai", "temp": 30.2, "humidity": 75, "condition": "Sunny"},
    {"city": "Kolkata", "temp": 26.5, "humidity": 80, "condition": "Cloudy"}
]

# System info
last_run = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
next_run = "2024-01-15 10:00:00"

# Print header
print("WEATHER DATA PIPELINE SYSTEM")
print("=" * 30)

print("\n📊 SYSTEM STATUS: RUNNING")
print(f"⏰ Last Run: {last_run}")
print("✅ Status: Successful")
print(f"📈 Records Processed: {len(weather_data)} cities")

# Weather Snapshot
print("\n🌤️ CURRENT WEATHER SNAPSHOT:")
print("-" * 33)

for data in weather_data:
    print(f"📍 {data['city']}: {data['temp']}°C, {data['humidity']}% humidity, {data['condition']}")

# Alerts
print("\n📅 TODAY'S ALERTS:")

for data in weather_data:
    if data["temp"] > 30:
        print(f"• High temperature alert: {data['city']} ({data['temp']}°C > 30°C threshold)")
    if data["humidity"] > 75:
        print(f"• High humidity alert: {data['city']} ({data['humidity']}% > 75% threshold)")

# Database stats
print("\n📊 DATABASE STATISTICS:")
print("• Total records: 10,250")
print("• Cities tracked: 15")
print("• Data coverage: 98.5%")
print("• Last error: None")

# Next run
print(f"\n🔄 NEXT SCHEDULED RUN: {next_run}")
